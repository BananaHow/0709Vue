<script>
export default{
    data(){
        return{
            bean:0,
        }
    },
    computed:{
        bottles(){
            return `${this.bean * 50}ml`;
        }
    }

}
</script>

<template>
<h1>變數 bean : {{ this.bean }}</h1>
<button type="button" @click="this.bean++">BTN</button>
<h2>假的數 bottles : {{ this.bottles }}</h2>
</template>

<style>

</style>