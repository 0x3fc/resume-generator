<template>
    <div class="card">
        <div class="container" style="user-select: none;">
            <!-- Name + Time -->
            <h3 style="float: left;">
                <a :href="link" target="_blank">
                    {{ company }}
                </a>
            </h3>
            <h3 style="float: right;">
                {{ from }} <span class="light-color">⤏</span> {{ to }}
            </h3>
            <!-- Title + Location -->
            <p style="clear: both; float: left;">
                {{ title }}
            </p>
            <p style="float: right;">
                <i class="fas fa-map-marker-alt"></i>
                {{ location }}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        company: String,
        link: String,
        location: String,
        title: String,
        from: String,
        to: String
    }
}
</script>

<style>

</style>
