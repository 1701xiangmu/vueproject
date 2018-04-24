<template>
  <header>
    <div class="swiper-container Head">
      <div class="swiper-wrapper">
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner1.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner2.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner3.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner4.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner5.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner6.jpg"/>-->
        <!--</div>-->
        <!--<div class="swiper-slide">-->
          <!--<img src="../../assets/img/index-banner7.jpg"/>-->
        <!--</div>-->
        <header-banner-img  key="ind" :img="n" v-for="(n,ind) in imgList"></header-banner-img>
      </div>
      <!-- Add Pagination -->
        <div class="swiper-pagination Btn"></div>
    </div>

  </header>
</template>

<script>
  import HeaderBannnerImg from "./HeaderBannerImg";
  import Swiper from  "swiper";
  import "../../../node_modules/swiper/dist/css/swiper.min.css";
  // import axios from 'axios';
  export default {
    //name: 'HeaderBannnerImg',
    props:["imgList"],
    components:{
      HeaderBannnerImg
    },
    mounted:function(){
      var swiper = new Swiper('.Head', {
        pagination: {
          el: '.swiper-pagination',
        },
        paginationClickable: true,
//        slidesPerView: 1,
//        spaceBetween: 20,
//        centeredSlides: true,
        autoplay: true,
//        autoplayDisableOnInteraction: false,
        //循环播放
        loop: true
      });

    },
    // data(){
    //   return {
    //     imgList:[]
    //   }
    // },
    // created:function(){
    //   // axios.get('/msg')
    //   //   .then(function (res) {
    //   //     this.imgList=res.data.img;
    //   //     console.log(res.data.img)
    //   //   })
    //   //   .catch(function (err) {
    //   //     console.log(err);
    //   //   });
    //     this.btn_ajax();
    // },
    // methods:{
    //   btn_ajax:function(){
    //
    //     this.$http({
    //       method:'get',
    //       url:'/msg',
    //       params: {                    //需要发送的数据
    //         // name: 'zhangwenwu2',
    //         // age: '15'
    //       }
    //     }).then(function (res) {
    //        var res = JSON.parse(res);
    //
    //        this.imgList=res.data.img;
    //       console.log(res.data.img)
    //     }).catch(function (err) {
    //         console.log(err);
    //       });
    //   }
    // }
  }
</script>

<style scoped>
  /*-----------头部start---------------------*/
  header {
    display: flex;
    position: relative;
    width: 100%;
    height: 100%;
    background: #eee;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 14px;
    color: #000;
    margin: 0;
    padding: 0; }

  .swiper-container {
    width: 100%;
    height: 100%; }

  .swiper-pagination .swiper-pagination-bullet-active {
    background: #0bca97; }

  .Btn .swiper-pagination-bullet-active {
    background: #9e9e9e; }

  .swiper-slide {
    width: 100%;
    height: 4.88889rem;
    text-align: center;
    font-size: 0.25rem;
    background: #fff;
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center; }
  .swiper-slide img {
    width: 100%;
    height: 100%; }
  .swiper-container {
    width: 100%;
    position: relative;
    background: white;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 0.14rem;
    color: #000;
    margin: 0;
    padding: 0; }

  .swiper-slide {
    text-align: center;
    font-size: 0.14rem; }

  .swiper-slide img {
    width: 100%;
    height: 100%; }

</style>
