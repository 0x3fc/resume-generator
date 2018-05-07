<template>
    <div>
        <h2>Volunteer Experience</h2>
        <div class="center-flex" v-for="experience in experiences" :key="experience.from">
            <experience
                :company="experience.company"
                :link="experience.link"
                :location="experience.location"
                :title="experience.title"
                :from="experience.from"
                :to="experience.to">
            </experience>
        </div>
    </div>
</template>

<script>
import Experience from '../templates/Experience';

export default {
    props: {
        experiences: Array
    },
    components: {
        Experience
    }
}
</script>

<style>

</style>
