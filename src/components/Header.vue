<script>
import { RouterLink } from 'vue-router'
export default{
    components:{
        RouterLink
    }
}
</script>

<template>
    <div class="headerArea">
        <RouterLink class="routeItem" to="/" >Home</RouterLink>
        <RouterLink class="routeItem" to="/VtextAndVmodel">VtextAndVmodel</RouterLink>
        <RouterLink class="routeItem" to="/VforAndVbind">VforAndVbind</RouterLink>
    </div>
</template>

<style scoped lang="scss">
.headerArea{
    width: 100%;
    height: 100%;
    background: rgb(66, 100, 135);
    display: flex;
    align-items: center;
    .routeItem{
        margin: 0 3%;
        font-size: 36px;
        color:white;
        text-decoration: none;
        cursor: pointer;
    }

}</style>
