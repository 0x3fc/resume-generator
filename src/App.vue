<template>
    <div id="app">
        <app-template></app-template>
        <!-- <mono-print></mono-print> -->
    </div>
</template>

<script>
import AppTemplate from './templates/App';
import MonoPrint from './templates/MonoPrint';

export default {
    components: {
        AppTemplate,
        MonoPrint
    }
}
</script>

<style>
@import './themes/midori.css';
</style>
