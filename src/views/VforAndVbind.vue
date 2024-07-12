<script>
import vfor from '../components/VforComponent.vue';
import vbindCom from '../components/VbindComponent.vue';
export default {
    data(){
        return{
            selectVal:"",
        }
    },
    components: {
        vfor,
        vbindCom
    }
}
</script>

<template>
    <div class="showArea">
        <select v-model="this.selectVal">
            <option value="vfor">vfor</option>
            <option value="vbind">vbind</option>
        </select>
        <vfor v-if="this.selectVal == 'vfor'"/>
        <vbindCom v-else/>
    </div>
</template>

<style scoped lang="scss">
.showArea{
    width: 60%;
    height:100%;
    overflow-y:scroll;
}
</style>