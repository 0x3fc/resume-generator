<template>
    <div class="card">
        <div class="container moreonhover">
            <h3 style="float: left;">
                <a :href="link" target="_blank">{{ name }}</a><span v-html="parseDemo"></span>
            </h3>
            <spacer style="marginRight: 15px;"></spacer>
            <template v-for="tag in tags">
                <tag :key="tag">{{ tag }}</tag>
            </template>
            <div style="clear: both;">
                <span style="user-select: none;">{{ description }}</span>
                <div class="more" id="img">
                    <carousel :per-page="1">
                        <template v-for="picture in pictures">
                            <slide :key="picture">
                                <img :src="picture" style="height: auto; width: 100%; marginTop: 10px;">
                            </slide>
                        </template>
                    </carousel>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';

export default {
    props: {
        name: String,
        tags: Array,
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
