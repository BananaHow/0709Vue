<script>
export default {
    data() {
        return {

        }
    },
    props: [
        "giveChildMsg",
        "giveChildObj", 
    // 若父層使用 v-bind 自動解構, 則要把物件屬性名稱寫在這告知子層
        "name", 
        "type"
    ]
}
</script>

<template>
    <h1>這邊是子層:{{ this.giveChildMsg }}</h1>
    <input type="text" v-model="this.giveChildObj">
    <h3>{{this.giveChildObj }}</h3>
    <h3>{{ this.type }}</h3>
</template>

<style scoped lang="scss"></style>