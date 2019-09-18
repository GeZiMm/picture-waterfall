<template>
    <div id="app">
        <!-- 瀑布流组件 -->
        <PictureWaterfall/>
    </div>
</template>

<script>
    import PictureWaterfall from "./components/PictureWaterfall.vue";

    export default {
        name: "app",
        components: {
            PictureWaterfall
        },
        data() {
            return {};
        }
    };
</script>

<style>
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
