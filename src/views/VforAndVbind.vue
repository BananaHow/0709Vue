<script>
import vfor from '../components/VforComponent.vue';
import vbindCom from '../components/VbindComponent.vue';
export default {
    components: {
        vfor,
        vbindCom
    }
}
</script>

<template>
    <div class="showArea">
        <vfor />
        <vbindCom />
    </div>
</template>

<style scoped lang="scss">
.showArea{
    width: 60%;
    height:100%;
    overflow-y:scroll;
}
</style>