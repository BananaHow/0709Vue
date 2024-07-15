<script>
export default {
    data() {
        return {
            point: 0,
            ntd: 0,
        }
    },
    watch: {
        point() {
            this.ntd = this.point * 10;
        }
    },
    methods: {
        arrTest() {
            let arr = [1, 2, 3, 4, 5, 6]
            arr.forEach((item) => {
                console.log(item);
                if (item == 4) {
                    return
                }
            })

            try {
                let arr = [1, 2, 3, 4, 5, 6]
                arr.forEach((item) => {
                    console.log(item);
                    if (item == 4) {
                        throw new Error("到四了")
                    }
                })
            } catch (e) {
                this.$swal({
                    icon: "success",
                    title: e.message,
                    showConfirmButton: false,
                    timer: 1500
                });
            }
        }
    },
    created() {
        this.arrTest()
    }
}
</script>

<template>
    <h1>變數 point : {{ this.point }}</h1>
    <button type="button" @click="this.point++">BTN</button>
    <h2>變數 ntd : {{ this.ntd }}</h2>

</template>

<style></style>