<template>
  <div class="icons">
      <swiper>
          <swiper-slide v-for="(page, index) in pages" :key="index">
            <div
                class="icon"
                v-for="icon in page"
                :key="icon.id"
            >
                <div class="icon-img">
                    <img class="icon-img-content" :src="icon.imgUrl">
                </div>
                <p class="icon-text">{{icon.text}}</p>
            </div>
          </swiper-slide> 
      </swiper>  
  </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data() {
        return {
            iconList: [
                {id:1, imgUrl: 'https://picbed.qunarzz.com/f5e5770393d759578962e53ee67798c8.png', text: '海外酒店'},
                {id:2, imgUrl: 'https://picbed.qunarzz.com/a36d2288f19e54562338f4d8ef986288.png', text: '低价机票'},
                {id:3, imgUrl: 'https://picbed.qunarzz.com/377db8cb2143aebf01869c9baad3d325.png', text: '汽车船票'},
                {id:4, imgUrl: 'https://picbed.qunarzz.com/ae617a31e0bd5803d76918b817f6d942.png', text: '自由行'},
                {id:5, imgUrl: 'https://picbed.qunarzz.com/1316dc82d1ce6259686d5a68880e5a9d.png', text: '攻略'},
                {id:6, imgUrl: 'https://picbed.qunarzz.com/01d2f57f920666364197a850dab859a8.png', text: '民宿客栈'},
                {id:7, imgUrl: 'https://picbed.qunarzz.com/83af731055e121a3251690b225327b56.png', text: '专车自驾'},
                {id:8, imgUrl: 'https://picbed.qunarzz.com/c65b3bb7571a6bd62df669213e44b84d.png', text: '一日游'},
                {id:9, imgUrl: 'https://picbed.qunarzz.com/5b6737be49ca243072ca614f07803b83.png', text: '赚信用卡'},
                {id:10, imgUrl: 'https://picbed.qunarzz.com/1e107321f5396ea4994cd832232ecf8a.png', text: '旅游团友'},
                {id:11, imgUrl: 'https://picbed.qunarzz.com/f6bb08a239ce1b038204120a8d1e4669.png', text: '特惠酒店'},
                {id:12, imgUrl: 'https://picbed.qunarzz.com/3a08f360e958ccb2b947049387873ace.png', text: '借钱'},
                {id:13, imgUrl: 'https://picbed.qunarzz.com/19b4f6d2fabd617789fa5aad65b249da.png', text: '白金卡'},
                {id:14, imgUrl: 'https://img1.qunarzz.com/order/comp/2007/23/734c3c62d2adce02.png', text: '行程设计'},
                {id:15, imgUrl: 'https://picbed.qunarzz.com/25e3b9f17a21a6e0113c57a23ffccde4.png', text: '周末游'},
            ]
        }
    },
    computed: {
        pages() {
            const pages = []
            let pageNum = 8
            for(let page=0;page * pageNum < this.iconList.length;page++) {
                pages[page] = [...this.iconList.slice(page*pageNum, (page+1)*pageNum)]
            }
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~css/variables'
    @import '~css/mixins'
    .icons >>> .swiper-container
        height: 0
        padding-bottom: 50%
    .icon
        overflow: hidden
        position: relative
        width: 25%
        height: 0
        padding-bottom: 25%
        float: left
        .icon-img
            position: absolute
            top: 0
            left: 0
            right: 0
            bottom: .44rem
            borderSizing border-box
            padding: .1rem
            .icon-img-content
                display: block
                margin: 0 auto
                height: 100%
        .icon-text
            position: absolute
            left: 0
            right: 0
            bottom: 0
            height: .44rem
            line-height: .44rem
            color: $darkTextColor
            text-align: center
            ellipsis()

</style>