<template>
    <div id="app" class="container">
        <heading></heading>
        <projects></projects>
        <work-experience></work-experience>
        <volunteer-experience></volunteer-experience>
        <education></education>
        <skills></skills>
        <logo></logo>
    </div>
</template>

<script>
import Heading from './components/Heading';
import Projects from './components/Projects';
import WorkExperience from './components/WorkExperience';
import VolunteerExperience from './components/VolunteerExperience';
import Education from './components/Education';
import Skills from './components/Skills';
import Logo from './components/Logo';

export default {
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
@import './themes/green-resume.css';
</style>
