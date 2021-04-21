<template>
    <el-rate
        v-model="value"
        disabled
        show-score
        text-color="#ff9900"
        score-template="">
    </el-rate>
</template>

<script>
export default {
    props: ['rating'],
    data() {
        return {
            value: this.rating
        }
    }
}
</script>

<style scoped>

</style>