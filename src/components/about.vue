<template>
  <section class="w1200">
    <h1>About me</h1>
    <article class="profile_wrap">
      <div class="profile_img">
        <div></div>
      </div>
      <div class="profile_contents">
          <swiper
    :pagination="true"
    :navigation="true"
    :modules="modules"
    class="mySwiper"
  >
            <swiper-slide>
              <div class="contents">
                <h3 class="slide_title">Profile</h3>
                <table>
                  <tr>
                    <td class="item_title">이름 :</td>
                    <td>박현민</td>
                  </tr>
                  <tr>
                    <td class="item_title">생년월일 :</td>
                    <td>1990.04.24</td>
                  </tr>
                  <tr>
                    <td class="item_title">주소 :</td>
                    <td>서울시 도봉구</td>
                  </tr>
                  <tr>
                    <td class="item_title">학력 :</td>
                    <td>월계고등학교 - 대진대학교 일본학과</td>
                  </tr>
                  <tr>
                    <td class="item_title">수료 :</td>
                    <td>
                      <p>그린컴퓨터아카데미 노원캠퍼스</p>
                      <p>[디지털컨버전스]스마트_뷰(Vue) 활용 프론트엔드 웹개발자 양성과정</p>
                    </td>
                  </tr>
                  <tr>
                    <td class="item_title">자격증 :</td>
                    <td>
                      <p>컴퓨터 활용 능력 1급</p>
                      <p>JLPT(일본어 능력시험) N1</p>
                      <p>GTQ 1급</p>
                      <p>운전면허증 1종 보통</p>
                    </td>
                  </tr>
                </table>
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="contents"></div>
              <h3 class="slide_title">Carrer</h3>
              <span class="line"></span>
              <ul class="carrer_contents">
                <li>
                  <span>2009.01 ~ 2011.06</span>
                  <span>보나쿠아 씨푸드 레스토랑 아르바이트 <em>(2년 5개월)</em></span>
                </li>
                <li>
                  <span>2011.06 ~ 2013.09</span>
                  <span>모락 광화문점 아르바이트 <em>(2년 3개월)</em></span>
                </li>
                <li>
                  <span>2014.02 ~ 2015.02</span>
                  <span>워킹홀리데이 <em>(일본 오사카 지역)</em></span>
                </li>
                <li>
                  <span>2015.03 ~ 2016.03</span>
                  <span>모락 광화문점 아르바이트 <em>(1년)</em></span>
                </li>
                <li>
                  <span>2016.04 ~ 2019.10</span>
                  <span>미쉘트레블 <em>(3년 7개월)</em></span>
                </li>
                <li>
                  <span>2020.02 ~ 2020.07</span>
                  <span>드림원격평생교육원 <em>(6개월)</em></span>
                </li>
                <li>
                  <span>2020.07 ~ 2022.01</span>
                  <span>클라리파이 <em>(1년 6개월)</em></span>
                </li>
              </ul>
            </swiper-slide>
          </swiper>
      </div>
      <button class="resume_btn btn" @click="resume = true">이력서</button>
      <div class="resumeFull" v-if="resume == true" @click="resume = false">
        <resumeOpen></resumeOpen>
      </div>
    </article>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import { Navigation } from "swiper";
import { Pagination } from "swiper";
import resumeOpen from './resume.vue'

export default {
    name: "about-page",
    data() {
        return {
            resume: false,
        };
    },
    components: {
        Swiper,
        SwiperSlide,
        resumeOpen
    },
    setup() {
    return {
      modules: [Pagination, Navigation],
    };
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.profile_wrap {
  display: flex;
  align-items:center;
  position: relative;
}

.profile_img {
  width:30%;
}

.profile_img>div {
  width: 100%;
  padding-bottom: 121.5%;
  background-image: url('../assets/profile.png');
  background-repeat: no-repeat;
  background-size: cover;
}


.swiper-slide {
  padding: 0 70px;
  box-sizing: border-box;
}

.profile_contents {
  width:70%;
}

.slide_title {
  font-size: 19px;
  font-weight: 600;
  margin-bottom: 16px;
}

/***********************profile***************************/

table {
  border-collapse: separate;
  border-spacing: 0 16px;
}

.item_title {
  width: 80px;
  text-align: justify;
}

/***********************carrer***************************/

.carrer_contents>li {
  padding: 10px 0;
  box-sizing: border-box;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.carrer_contents>li>span:first-child {
  padding-right: 30px;
  position: relative;
}

.carrer_contents>li>span:first-child::after {
  content: "";
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background-color: #FFA619;
  position: absolute;
  top: 50%;
  transform: translate(0, -50%);
  right: 11px;
}

.carrer_contents::before {
  content: "";
  width: 1px;
  height: 300px;
  background-color: #e9e9e9;
  display: block;
  position: absolute;
  top: 50;
  left: 218px;
}



/***********************이력서버튼***************************/

.resume_btn {
  position: absolute;
  bottom: 0;
  right: 50px;
}

/***********************스와이퍼 화살표 컬러**************************/

.swiper {
    --swiper-navigation-color: #FFA619;
    --swiper-pagination-color: #FFA619;
    --swiper-pagination-bullet-inactive-color:#e9e9e9; 
    --swiper-pagination-bullet-inactive-opacity: 1;
}


@media screen and (max-width: 768px) {
    .profile_wrap {
      flex-direction: column-reverse;
    }

    .profile_img {
      width:60%;}

    .profile_contents {
      width:100%;}

    .resume_btn {
      top: 0;
      right: 0;
    }

    /*스와이퍼*/
    .swiper-slide {
      padding: 0;
    }

    .carrer_contents::before {
      left: 147px;
    }

    .swiper-pagination {
      position: relative;
      bottom: 0px;
    }

}

@media screen and (max-width: 420px) {

  .carrer_contents>li {
  padding: 10px 0;
  box-sizing: border-box;
  white-space: pre-wrap;
}

  .carrer_contents>li>span:first-child {
    display: none;
  }

  .carrer_contents>li>span:last-child>em {
    display: inline-block;
  }

  .carrer_contents>li>span:first-child::after {
    display: none;
  }

  .carrer_contents::before{
    display: none;
  }

}




</style>
