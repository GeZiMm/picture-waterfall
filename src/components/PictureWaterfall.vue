<template>
<!--    参考https://github.com/lfyfly/vue-waterfall-easy/blob/master/README-CN.md-->
    <vueWaterfallEasy ref="waterfall"
                      :imgsArr="imgArr"
                      :height="200"
                      :gap="20"
                      @scrollReachBottom="getData"
    >
        <div slot="waterfall-over">已经到底了</div>
    </vueWaterfallEasy>
</template>

<script>
    import VueWaterfallEasy from "vue-waterfall-easy";

    export default {
        name: "PictureWaterfall",
        components: {VueWaterfallEasy},
        data() {
            return {
                imgArr: [{src: require('../assets/1.jpg'), href: ''}, {src: require('../assets/3.jpg'), href: ''}],
                count: 2,
            };
        },
        methods: {
            getData() {
                if (this.count === 20) {
                    this.$refs.waterfall.waterfallOver()
                } else {
                    this.count += 1;
                    this.imgArr.push({src: require('../assets/' + this.count + '.jpg'), href: ''})
                }
            }
        }
    };
</script>

<style scoped>
</style>
