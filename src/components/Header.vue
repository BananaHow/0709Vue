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
        <RouterLink class="routeItem" to="/VonAndVifAndVshow">VonAndVifAndVshow</RouterLink>
        <RouterLink class="routeItem" to="/Props">Props</RouterLink>
        <RouterLink class="routeItem" to="/Emit">Emit</RouterLink>
        <RouterLink class="routeItem" to="/WatchAndComputed">WatchAndComputed</RouterLink>
    </div>
</template>

<style scoped lang="scss">
.headerArea{
    width: 100%;
    height: 100%;
    background: rgb(66, 100, 135);
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    .routeItem{
        margin: 0 1%;
        font-size: 2dvw;
        color:white;
        text-decoration: none;
        cursor: pointer;
    }

}</style>
