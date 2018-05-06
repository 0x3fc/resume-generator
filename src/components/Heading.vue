<template>
    <div>
        <heading
            :name="heading.name"
            :subheaders="heading.subheaders">
        </heading>
        <hr />
    </div>
</template>

<script>
import Heading from '../templates/Heading';

export default {
    props: {
        heading: Object
    },
    components: {
        Heading
    }
}
</script>

<style>

</style>
