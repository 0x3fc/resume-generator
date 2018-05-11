<template>
    <div class="container">
        <div class="container">
            <heading :heading="heading"></heading>
            <p>
                The resume contains a lot of links, view the website version on 
                <a href="http://resume.senhung.net" target="_blank">http://resume.senhung.net</a>. Thank you!
            </p>
            <skills :skills="skills"></skills>
            <projects :projects="projects"></projects>
            <p>
                View my other 10+ projects on 
                <a href="http://resume.senhung.net" target="_blank">http://resume.senhung.net</a> or
                <a href="http://github.com/senhungwong" target="_blank">http://github.com/senhungwong</a>. Thank you!
            </p>
            <work-experience :experiences="workExperiences"></work-experience>
            <volunteer-experience :experiences="volunteerExperiences"></volunteer-experience>
            <education :educations="educations"></education>
            <logo></logo>
        </div>
    </div>
</template>

<script>
import Heading from '../components/Heading';
import Projects from '../components/Projects';
import WorkExperience from '../components/WorkExperience';
import VolunteerExperience from '../components/VolunteerExperience';
import Education from '../components/Education';
import Skills from '../components/Skills';
import Logo from '../components/Logo';
import data from '../../data.json';

export default {
    data() {
        return {
            heading: data.heading,
            workExperiences: data.work_experiences,
            volunteerExperiences: data.volunteer_experiences,
            educations: data.educations,
            skills: data.skills
        }
    },
    components: {
        Heading,
        Projects,
        WorkExperience,
        VolunteerExperience,
        Education,
        Skills,
        Logo
    },
    computed: {
        projects() {
            let projects = data.projects.slice(0, 4);
            for (let i = 0; i < projects.length; i++) {
                projects[i].demo = null;
            }
            return projects;
        }
    }
}
</script>

<style>

</style>
