<template lang="html">
    <!-- 这个作为全局页面加载文件 -->
    <div>
        <myHeader/>
        <Slider/>
        <Novice />
        <Borrow />
        <Money />
        <Product />
        <Life />
        <myFooter/>
        <Navbar/>
    </div>
</template>

<script>
// vue保留Header标签关键字，所以我们不能直接使用
import myHeader from "../public/header.vue"
import myFooter from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import Life from "./life.vue"

export default {
    components: {
        myHeader,
        Slider,
        Novice,
        Borrow,
        Money,
        Product,
        Life,
        myFooter,
        Navbar,
    },
}

</script>

<style>
body {
    background-color: #f5f5f5;
}
</style>
