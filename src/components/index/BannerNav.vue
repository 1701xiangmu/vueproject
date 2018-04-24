<template>
  <div class="swiper-container Nav">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <div class="nav">
          <ul class="nav-ul1">
            <li class="nav-ul1-li1"><img src="../../assets/img/index-nav1.png"/><br><span>机票</span></li>
            <li class="nav-ul1-li2"><img src="../../assets/img/index-nav2.png"/><br><span>酒店</span></li>
            <li class="nav-ul1-li3"><img src="../../assets/img/index-nav3.png"/><br><span>机+酒</span></li>
            <li class="nav-ul1-li4"><img src="../../assets/img/index-nav4.png"/><br><span>全球购</span></li>
            <!--<cqhk-nav-banner-img key="index" :pro="n" v-for="(n,index) in imgNa.img01"></cqhk-nav-banner-img>-->
          </ul>
        </div>
      </div>
      <div class="swiper-slide">
        <div class="nav">
          <ul class="nav-ul1">
            <li class="nav-ul1-li2"><img src="../../assets/img/index-nav10.png"/><br><span>行程规划</span></li>
            <li class="nav-ul1-li6"><img src="../../assets/img/index-nav11.png"/><br><span>包车游</span></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <!--<cqhk-nav-banner-img key="index" :pro="n" v-for="(n,index) in imgNa.img02"></cqhk-nav-banner-img>-->
          </ul>
        </div>
      </div>
    </div>
    <div class="swiper-pagination"></div>
  </div>
</template>

<script>
  import Swiper from  "swiper";
  import "../../../node_modules/swiper/dist/css/swiper.min.css";
    export default {
        name: "banner-nav",
      mounted:function(){
        var swiper = new Swiper('.Nav', {
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
    }
</script>

<style lang="scss" scoped>
  /*----------------------------nav---------------------------------*/
  .nav{
    width:100%;
    height:6.5rem;
    .nav-ul1{
      width:100%;
      height:3.24rem;
      display: flex;
      display: -webkit-flex;
      justify-content: flex-start;
      align-items: center;
      flex-wrap: wrap;
      .nav-ul1-li1 img{
        background: #e29f37;
      }
      .nav-ul1-li2{
        img{
          background:#cc2827;
        }
      }
      .nav-ul1-li3{
        img{
          background:#7542dd;
        }
      }
      .nav-ul1-li4{
        img{
          background:#2ec961;
        }
      }
      .nav-ul1-li5{
        img{
          background:#fbc800;
        }
      }
      li{
        width: 25%;
        height:2.31rem;
        position: relative;
        text-align: center;
        margin-top:0.56rem;
        img{
          width:1.48rem;
          height:1.48rem;
          border-radius: 50%;
        }
        span{
          display: block;
          margin-top:0.2rem;
          font-size:0.3rem;
        }
      }
    }

    .nav-ul2-li6{
      width:2.5rem;
      img{
        background: #1593e0;
      }

    }
    .nav-ul2-li7{
      width:2.2rem;
      img{
        background: #e545e5;
      }

    }
    .nav-ul2-li8 img{
      background: #15bbf9;
    }
    .nav-ul2-li9 img{
      background: #ec4386;
    }
    .nav-ul2-li10 img{
      background: #ff4c55;
    }

    li{
      width:2.3rem;
      height:2.31rem;

      position: relative;
      text-align: center;
      img{
        width:1.48rem;
        height:1.48rem;
        border-radius: 50%;
        background: #e29f37;
      }
      span{
        display: block;
        margin-top:0.2rem;
        font-size:0.3rem;
      }
    }

  }
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
