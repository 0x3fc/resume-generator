<template>
    <div class="card moreonhover" style="user-select: none;">
        <div class="container">
            <!-- Name + Time -->
            <h3 style="float: left;">
                <a :href="link" target="_blank">
                    {{ place }}
                </a>
            </h3>
            <h3 style="float: right;">
                {{ from }} <span class="light-color">⤏</span> {{ to }}
            </h3>
            <!-- Title/Program + Location -->
            <p style="clear: both; float: left;">
                {{ position }}
            </p>
            <p style="float: right;">
                <i class="fas fa-map-marker-alt"></i>
                {{ location }}
            </p>
        </div>
        <div class="container more" style="clear: both;">
            <ul v-for="item in more" :key="item">
                <li>{{item}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        place: String,
        link: String,
        location: String,
        position: String,
        from: String,
        to: String,
        more: Array
    }
}
</script>

<style>

</style>
