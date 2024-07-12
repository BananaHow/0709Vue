<script>
import propChild from '../components/PropsComponents.vue'
export default {
    data() {
        return {
            parentMsg: "parentVal",
            parentObj: {
                name: "米諾",
                type: "臘腸"
            }
        }
    },
    components: {
        propChild,
    }
}
</script>

<template>
    <h1>這邊是父層:{{ this.parentMsg }}</h1>
    <h1>父層物件:{{this.parentObj}}</h1>
    <!-- 務必遵循單一資訊流 -->
    <!-- 若傳子層的資料型態為物件, 一定要拆解或是使用 v-bind 自動把資料解構傳遞 -->
    <propChild v-bind:giveChildMsg="this.parentMsg" :giveChildObj="this.parentObj.name"  v-bind="this.parentObj"/>

</template>

<style scoped lang="scss"></style>