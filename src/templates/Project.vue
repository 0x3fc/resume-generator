<template>
    <div class="card">
        <div class="container moreonhover">
            <h3><a :href="link" target="_blank">{{ name }}</a><span v-html="parseDemo"></span></h3>
            <span style="user-select: none;">{{ description }}</span>
            <div class="more">
                <carousel>
                    <template v-for="picture in pictures">
                        <slide :key="picture">
                            <img :src="picture" style="height: auto; width: 100%;">
                        </slide>
                    </template>
                </carousel>
            </div>
        </div>
    </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
    props: {
        name: String,
        link: String,
        description: String,
        demo: String,
        pictures: Array
    },
    components: {
        Carousel,
        Slide
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
