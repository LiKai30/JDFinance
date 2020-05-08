<template lang="html">
    <div>
        <myHeader/>
        <Slider/>
        <Ada/>
        <Money/>
        <Adb/>
        <Finance/>
        <Adc/>
        <myFooter cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import myHeader from "../public/header.vue"
import myFooter from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./mslider.vue"
import Ada from "./ada.vue"
import Money from "./money.vue"
import Adb from "./adb.vue"
import Finance from "./finance.vue"
import Adc from "./adc.vue"
export default {
    components: {
        myHeader,
        Slider,
        Ada,
        Money,
        Adb,
        Finance,
        Adc,
        myFooter,
        Navbar,
    },
}
</script>

<style lang="scss">
  .mfooter{
    margin-top: 0!important;
    ul{
      li:first-child{
        display: none;
      }
    }
  }
</style>
