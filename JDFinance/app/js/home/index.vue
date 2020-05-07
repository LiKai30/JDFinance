<template lang="html">
    <!-- 这个作为全局页面加载文件 -->
    <div>
        <myHeader/>
        <Slider/>
    </div>
</template>

<script>
// vue保留Header标签关键字，所以我们不能直接使用
import myHeader from "../public/header.vue"
import Slider from "./hslider.vue"
export default {
    components: {
        myHeader,
        Slider,
    },
}

</script>

<style lang="scss" module>
</style>
