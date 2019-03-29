<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>


      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>

<script>
  export default {
    name: "HomeSwiper",
    data(){
      return{
        swiperOption:{
          pagination:'.swiper-pagination',
          loop:true
        },
        swiperList:[{
          id:'0001',
          imgUrl:'//img.alicdn.com/imgextra/i4/127/O1CN01y4lNNL1CoCoFSO82d_!!127-0-luban.jpg'
        },{
          id:'0002',
          imgUrl:'//gw.alicdn.com/imgextra/i2/96/O1CN01N6rKtw1Ca0WyjHTYg_!!96-0-luban.jpg'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow:hidden
    width:100%
    height:0
    padding-bottom:33.5%
    .swiper-img
      width:100%
</style>