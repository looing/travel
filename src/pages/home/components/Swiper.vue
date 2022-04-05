<template>
    <div class="warpper">
        <swiper :options="swiperOption">
            <!-- 轮播图 -->
            <swiper-slide v-for="swiper in swiperList" :key="swiper.id">
                <img class="swiper-img" :src="swiper.imgUrl" :alt="swiper.description">
            </swiper-slide>

            <!-- 分页 -->
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data() {
        return {
            swiperOption: {
                pagination: ".swiper-pagination",
                loop: true
            },
            swiperList: [{
                id: 'img001',
                description: '千岛湖',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/2005/1c/1ccff2940b61484ba3.water.jpg_600x330_2b3f6ad1.jpg'
            }, {
                id: 'img002',
                description: '西湖',
                imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/87/87146cf32fa8635e90.water.png_600x330_54030989.png'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .warpper >>> .swiper-pagination-bullet-active
        background-color: #fff !important
    .warpper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 55%
        background-color: #ccc
        .swiper-img
            width: 100%
</style>