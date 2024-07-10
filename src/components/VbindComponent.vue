<script>
export default {
    data() {
        return {
            imgArr: [
                "https://tw.portal-pokemon.com/play/resources/pokedex/img/pm/0783062d0d860b8ae7d8e859241a700359c4d981.png",
                "https://tw.portal-pokemon.com/play/resources/pokedex/img/pm/3755f6d1176c7f8c64f663dae13ef9f1406d007a.png",
                "https://tw.portal-pokemon.com/play/resources/pokedex/img/pm/0f94860cb73755f14d3930eeda4117f6d196c336.png"
            ],
            clsArr: [],
        }
    }
}
</script>

<template>
    <!-- v-bind 跟標籤的屬性雙向綁定 -->
    <!-- <img v-bind:src="item" alt="" v-for="item in this.imgArr"> -->
    <!-- v-bind:src 縮寫是 :src -->
    <div class="imgArea">
        <img :src="item" alt="" v-for="item in this.imgArr">
    </div>

    <label for="">Blue</label>
    <input type="checkbox" value="blue" v-model="this.clsArr">
    <label for="">Large</label>
    <input type="checkbox" value="large" v-model="this.clsArr">
    <label for="">UnderLine</label>
    <input type="checkbox" value="underLine" v-model="this.clsArr">
    <h1 :class="this.clsArr">榮俊威武</h1>
</template>

<style scoped lang="scss">
.imgArea {
    width: 200px;
    height: 200px;
    overflow-y: scroll;

    img {
        max-width: 100%;
    }
}

.blue {
    color: blue;
}

.large {
    font-size: 64px;
}

.underLine {
    text-decoration: underline;
}
</style>