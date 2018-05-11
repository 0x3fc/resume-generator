<template>
    <div>
        <h2>Projects</h2>
        <div class="center-flex" v-for="project in projects" :key="project.name">
            <project 
                :name="project.name"
                :tags="project.tags"
                :link="project.link"
                :pictures="project.pictures"
                :description="project.description"
                :demo="project.demo">
            </project>
        </div>
    </div>
</template>

<script>
import Project from '../templates/Project';

export default {
    props: {
        projects: Array
    },
    components: {
        Project
    }
}
</script>

<style>

</style>
