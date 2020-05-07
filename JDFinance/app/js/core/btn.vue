<template>
    <div :class="[btnClass, cname]">
        <!-- 继承的实现：先有一个默认的类名，然后允许传递一个类名 -->
        <!-- 插槽是为了在具体使用的时候方便填充 -->
        <slot />
    </div>
</template>

<script>
export default {
    // 属性传递
    props: {
        cname: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            btnClass: "btn",
        }
    },
}
</script>

<style lang="scss">
@import "../../css/element.scss";

.btn{
    @include btn;
}

</style>
