<template>
    <div>
        <h2>Work Experience</h2>
        <div class="center-flex" v-for="experience in experiences" :key="experience.from">
            <work-experience
                :company="experience.company"
                :link="experience.link"
                :location="experience.location"
                :title="experience.title"
                :from="experience.from"
                :to="experience.to">
            </work-experience>
        </div>
    </div>
</template>

<script>
import WorkExperience from '../templates/WorkExperience';

export default {
    props: {
        experiences: Array
    },
    components: {
        WorkExperience
    }
}
</script>

<style>

</style>
