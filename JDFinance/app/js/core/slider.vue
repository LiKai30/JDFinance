<template lang="html">
    <section :class="cname">
        <!-- 需要考虑配置项的传递，也就是传参 -->
        <swiper :option="options" :not-next-tick="options.noNextTick">
            <!-- 填充有两种方式：slot和数组 但是使用插槽就必须使用swiper-slide，这样每次都的引入swiper-->
            <swiper-slide v-for="item in items" :key="item.href">
                <!-- 因为要跳转，所以使用router-link -->
                <router-link :to="{ name:item.href }">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
        </swiper>
    </section>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper"
export default {
    // 使用组件
    components: {
        Swiper,
        SwiperSlide,
    },
    props: {
        cname: {
            type: String,
            default: "",
        },
        options: {
            type: Object,
            // 任何一个对象都要写成return的形式
            default() {
                return {
                    autoplay: true,
                    loop: true,
                    pagination: {
                        el: ".swiper-pagination",
                    },
                    noNextTick: false,
                }
            },
            // 相当于
            // default:function(){
            //     return {}
            // }
        },
        items: {
            type: Array,
            default() {
                return []
            },
        },
    },
}
</script>

<style lang="css">
/* 引入样式文件 */
@import "~swiper/css/swiper.css";
</style>
