<template>
    <div>
        <h2>Education</h2>
        <div class="center-flex" v-for="education in educations" :key="education.name">
            <education
                :place="education.place"
                :link="education.link"
                :location="education.location"
                :program="education.program"
                :from="education.from"
                :to="education.to">
            </education>
        </div>
    </div>
</template>

<script>
import Education from '../templates/Education.vue';

export default {
    props: {
        educations: Array
    },
    components: {
        Education
    }
}
</script>

<style>

</style>
