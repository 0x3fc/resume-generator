<template>
    <div class="container">
        <heading :heading="heading"></heading>
        <projects :projects="projects"></projects>
        <work-experience :experiences="workExperiences"></work-experience>
        <volunteer-experience :experiences="volunteerExperiences"></volunteer-experience>
        <education></education>
        <skills></skills>
        <logo></logo>
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
            projects: data.projects,
            workExperiences: data.work_experiences,
            volunteerExperiences: data.volunteer_experiences
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
    }
}
</script>

<style>
@import '../themes/green-resume.css';
</style>
