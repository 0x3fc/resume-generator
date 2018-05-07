<template>
    <div class="card">
        <div class="container" style="user-select: none;">
            <h3 style="float: left;">{{ title }}:</h3>
            <span style="float: right;">{{ skillString }}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: String,
        skills: Array
    },
    computed: {
        skillString() {
            return this.skills.join(', ');
        }
    }
}
</script>

<style>

</style>
