<template>
    <div class="card" v-for="(item,index) in cardInfo" :key="index">
        <div class="card-image">
            <img :src="item.thumb" :alt="item.series">
        </div>
        <h6>{{item.series}}</h6>
    </div>
</template>

<script>
    import { dcComicsCardInfo } from '../assets/data/dc-comics';

    export default {
        name: 'CardComponent',
        data() {
            return {
                cardInfo: dcComicsCardInfo,
            }
        },
        mounted() {
            console.log(this.cardInfo)
        },
    }
</script>

<style lang="scss" scoped>
.card-image {
    max-width: 10rem;
    max-height: 10rem;
    overflow: hidden;
}
.card {
    width: calc((100% / 6) - 30px);
    height: auto;

    h6 {
        margin: 10px 0 25px;
    }
}
</style>