<script>
import emitChild from '../components/EmitComponents.vue'
export default {
    data(){
        return{
            getChildVal:"",
            childChagne:"parent"
        }
    },
    components: {
        emitChild,
    },
    methods:{
        childFun(params){
            console.log(params);
            this.getChildVal = params;
        }
    },
    beforeCreate(){
        console.log("beforeCreate");
    },
    created(){
        console.log("created");
    },
    beforeMount(){
        console.log("beforeMount");
    },
    mounted(){
        console.log("mounted");
    },
    beforeUpdate(){
        console.log("beforeUpdate");
    },
    updated(){
        console.log("update");
    },
    beforeUnmount(){
        console.log("beforeUnmount");
    },
    unmounted(){
        console.log("unmounted");
    }
}
</script>

<template>
    <emitChild @childMsg="this.childFun"
    v-model:fromChild="this.childChagne"/>
    <h2>{{ this.getChildVal }}</h2>
    <h2>{{ this.childChagne }}</h2>
</template>

<style></style>