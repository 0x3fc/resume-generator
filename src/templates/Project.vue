<template>
    <div class="card" @mouseover="active = true" @mouseleave="active = false">
        <div class="container">
            <h3><a :href="link" target="_blank">{{ name }}</a><span v-html="parseDemo"></span></h3>
            <span style="user-select: none;">{{ description }}</span>
            <div v-if="active">Images</div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        name: String,
        link: String,
        description: String,
        demo: String
    },
    data() {
        return {
            active: false
        }
    },
    computed: {
        parseDemo() {
            return this.demo ? ' <a href="' + this.demo + '" target="_blank">[Demo]</a>' : null;
        }
    }
}
</script>

<style>

</style>
