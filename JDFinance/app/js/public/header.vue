<template>
    <div :class="$style.header">
        <span :class="$style.left">
            <!-- 实际开发用router-link，这里写死 -->
            <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
        </span>
        <!-- 因为btn组件使用slot，所以这里直接这么写 -->
        <btn :class="$style.btnDownload">APP下载</btn>
    </div>
</template>

<script>
import btn from "../core/btn.vue"
export default {
    components: {
        btn,
    },
}
</script>


<style lang="scss" module>
.header {
    position:fixed;
    top: 0;
    left: 0;
    /* 这里让宽度变成了100% */
    right: 0;
    height: 100px;
    line-height: 100px;
    color:#666;
    font-size: 32px;
    background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
    background-size: auto 50%;
    z-index:100;
    .left {
        font-size: 28px;
        height:30px;
        line-height:30px;
        margin:17px 0 0 18px;
    }
    .btnDownload {
        font-size: 24px;
        float: right;
        border-width: 0;
        border-radius: 4px;
        padding: 0;
        margin:28px 24px 0 0;
        height: 56px;
        min-width:120px;
        line-height: 56px;
    }
}
</style>
