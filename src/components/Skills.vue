<template>
    <div>
        <h2>Skills</h2>
        <div class="center-flex" v-for="(skillSet, title) in skills" :key="title">
            <skill :title="title" :skills="skillSet"></skill>
        </div>
    </div>
</template>

<script>
import Skill from '../templates/Skill';

export default {
    props: {
        skills: Object
    },
    components: {
        Skill
    }
}
</script>

<style>

</style>
