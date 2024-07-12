<script>

export default{
    data(){
        return{
            vonTextOne:"vonTestOne",
        }
    },
    methods:{
        vonTestFun(){
            console.log(this.vonTextOne);
        },
        inputTestOn(){
            console.log("inputEvent");
        }
    }
}
</script>

<template>
    <button type="button" v-on:click="this.vonTestFun()">Btn</button>
    <button type="button" @click="this.vonTestFun()">Btn2</button>
    <input type="text" @input="this.inputTestOn()">

</template>

<style scoped lang="scss">

</style>