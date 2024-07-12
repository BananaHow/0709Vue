<script>
import vonCp from '../components/VonComponent.vue';
import vifAndVshowCp from '../components/VifAndVshowComponent.vue'
import modal from "../components/SlotModal.vue"
export default{
    components:{
        vonCp,
        vifAndVshowCp,
        modal,
    }
}
</script>

<template>
    
    <vonCp />
    <vifAndVshowCp />
    <modal>
        Funny
        <template v-slot:title>
            這是標題
        </template>
    </modal>
</template>

<style scoped lang="scss">

</style>