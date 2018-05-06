<template>
    <div class="card">
        <div @mouseover="active = true" @mouseleave="active = false">Hover over me!</div>
        <div class="animated bounceIn" v-if="active">Show</div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            active: false
        }
    }
}
</script>

<style>

</style>
