app.vue

<template>
    <div id="app">
        <cmp-footer></cmp-footer>
        <router-view></router-view>
    </div>
</template>

<script>
import Footer from "./components/Footer";

export default {
    name: "app",
    components: {
        "cmp-footer": Footer
    }
};
</script>

<style>
</style>