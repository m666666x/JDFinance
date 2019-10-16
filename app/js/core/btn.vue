<!--  -->
<template lang="html">
    <div :class="[btnClass,cname]">
        <slot/>
    </div>
</template>

<script>
export default {
    components: {},
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
<style lang='scss' scoped>
@import "../../css/element.scss";
.btn {
  @include btn;
}
</style>
