<template>
    <div>
        <h1>{{ name }}</h1>
        <div class="center-flex">
            <ul class="separator">
                <li v-for="subheader in subheaders" :key="subheader.text">
                    <a :href="subheader.link" :target="subheader.newpage ? '_blank' : null">
                        <i :class="subheader.icon"></i>
                        {{ subheader.text }}
                    </a>
                </li>
            </ul>
        </div>
        <hr />
    </div>
</template>

<script>
export default {
    props: {
        name: String,
        subheaders: Array
    }
}
</script>

<style>

</style>
