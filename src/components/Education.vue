<template>
    <div>
        <h2>Education</h2>
        <div class="center-flex" v-for="education in educations" :key="education.name">
            <experience
                :place="education.place"
                :link="education.link"
                :location="education.location"
                :position="education.program"
                :from="education.from"
                :to="education.to"
                :more="education.more">
            </experience>
        </div>
    </div>
</template>

<script>
import Experience from '../templates/Experience';

export default {
    props: {
        educations: Array
    },
    components: {
        Experience
    }
}
</script>

<style>

</style>
