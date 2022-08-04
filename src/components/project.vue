<template>
  <section class="w1200">
    <h1>project</h1>
    <article class="project_wrap">
      <div class="seomun">
        <div class="contents">
          <h3 class="mb16">서문시장 야시장</h3>
          <p class="mb16">제작기간 : 2022.03 ~ 2022.07</p>
          <p>참여율 : 100%</p>
          <div class="comment">
            <span>기존 사이트에서 부족했던 색감과 디자인의 통일성을 개선하고,</span>
            <span>사용자의 편의성을 고려하여 메인, 소개, 공지사항 페이지를 새롭게 제작했습니다.</span>
          </div>
          <div class="languages">
            <h5 class="size19">Language & Tool</h5>
            <div class="languages_icon">
              <img src="../assets/html.png">
              <img src="../assets/css.png">
              <img src="../assets/js.png">
              <img src="../assets/jquery.png">
              <img src="../assets/node.png">
              <img src="../assets/mysql.png">
              <img src="../assets/figma.png">
            </div>
          </div>
          <div class="project_btn seomun_linkbtn">
            <button class="btn mockup_btn" @click="seomunMockup = true">MOCKUP</button>
            <button class="btn web_btn" @click="gotoSeomun()">WEB</button>
          </div>
        </div>
        <div class="project_img seomun_img">
          <img src="../assets/seomun.png">
          <div class="m_btn seomun_btn">
            <button @click="seomun = true">MORE</button>
          </div>
        </div>
          <seomunDetail v-if="seomun == true" @click="seomun = false"></seomunDetail>
      </div>
      <div class="hilton">
        <hiltonDetail v-if="hilton == true" @click="hilton = false"></hiltonDetail>
        <div class="project_img hilton_img">
          <img src="../assets/hilton.png">
          <div class="m_btn hilton_btn">
            <button @click="hilton = true">MORE</button>
          </div>
        </div>
        <div class="contents">
          <h3 class="mb16">밀레니엄 힐튼 서울</h3>
          <p class="mb16">제작기간 : 2022.05 ~ 2022.06</p>
          <p>참여율 : 30%</p>
          <div class="comment">
            <span>기존 사이트에서 부족했던 디자인 요소 및 편의성을 개선하고,</span>
            <span>콘텐츠를 추가하여 홈페이지를 새롭게 제작했습니다.</span>
          </div>
          <div class="languages">
            <h5 class="size19">Language & Tool</h5>
            <div class="languages_icon">
              <img src="../assets/html.png">
              <img src="../assets/css.png">
              <img src="../assets/js.png">
              <img src="../assets/jquery.png">
              <img src="../assets/node.png">
              <img src="../assets/mysql.png">
              <img src="../assets/figma.png">
            </div>
          </div>
          <div class="project_btn hilton_linkbtn">
            <button class="btn mockup_btn" @click="hiltonMockup = true">MOCKUP</button>
            <button class="btn web_btn" @click="gotoHilton()">WEB</button>
          </div>
      </div>
      </div>
    </article>
    <div class="Mockup hiltonMockup" v-if="hiltonMockup == true" @click="hiltonMockup = false">
      <div class="mockup_size"> 
        <img src="../assets/hiltonMockup.png">
      </div>
    </div>
    <div class="Mockup hiltonMockup" v-if="seomunMockup == true" @click="seomunMockup = false">
      <div class="mockup_size"> 
        <img src="../assets/seomunMockup.png">
      </div>
    </div>
  </section> 
</template>

<script>

import seomunDetail from './seomunDetail.vue'
import hiltonDetail from './hiltonDetail.vue'

export default {
  name: 'project-page',
  data() {
    return {
      hiltonMockup: false,
      seomunMockup: false,
      seomun: false,
      hilton: false,
    };
  },
  methods: {
      gotoHilton: function(){
      window.open("https://hiltonseoulfinal.herokuapp.com/", "_blank");
    }, 
    gotoSeomun: function(){
      window.open("https://seomunmarket.herokuapp.com/", "_blank");
    }
  },
  components: {
    seomunDetail,
    hiltonDetail
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.project_wrap>div {
  width: 100%;
  display: flex;
}

.project_wrap>div:first-child {
  margin-bottom: 200px;
}

/****************PC목업 이미지****************/

.project_img {
  display: flex;
  width: 50%;
}

.project_img>img {
  width: 100%;
}

/****************버튼***************/

.m_btn {
  display: none;
}

.m_btn>button {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  border: 1px solid #FFA619;
  background-color: #fff;
  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
  color: #FFA619;
  font-weight: 600;
  cursor: pointer;
}

.m_btn>button:hover {
  background-color: #FFA619;
  color: #fff;
}

/****************contents****************/

.contents {
  width: 50%;
  position: relative;
}

.contents>h3 {
  font-size: 33px;
  font-weight: 700;
}

.contents>p {
  font-size: 19px;
  font-weight: 600;
}

.comment {
  margin: 50px 0;
}

.comment>span {
  display: inline-block;
}

.languages>h5 {
  margin-bottom: 16px;
}

.languages_icon>img {
  width: 60px;
  height: 60px;
  margin-left: 15px;
}

.languages_icon>img:first-child {
  margin-left: 0;
}

.project_btn {
  position: absolute;
  bottom: 0;
}

.seomun_linkbtn {
  left: 0;
}

.hilton_linkbtn{
  right: 0;
}

.project_btn>button:first-child {
  margin-right: 24px;
}

.hilton>.contents {
  text-align: right;
}

/***************목업***************/

.Mockup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 99;
  padding: 30px;
  box-sizing: border-box;
  overflow-y: scroll;
}



.hiltonMockup img {
  width: 100%;
  border-radius: 10px;
}

@media screen and (max-width: 1200px) {

.project_wrap>.seomun {
  flex-direction: column-reverse;
}

.project_wrap>.hilton {
  flex-direction: column;
}

.project_img {
  width: 70%;
  margin: 0 auto 50px;
}

.contents {
  width: 100%;
  text-align: center;
}

.hilton>.contents {
  text-align: center;
}

.comment>span {
  display: block;
}

.project_btn {
  position: static;
  margin-top: 50px;
}



}

@media screen and (max-width: 768px) {


/****************PC목업 이미지****************/

.project_img {
  width: 100%;
  position: relative;
}

.project_img>img {
  position: relative;
  width: 100%;
  top: 0;
}

.seomun_img>img {
  left: -20%;
}

.hilton_img>img {
  right: -20%;
}

/****************버튼***************/

.m_btn {
  display: block;
  position: absolute;
  width: 20%;
  top: 50%;
  transform: translate(0, -50%);
}

.m_btn>button {
  display: block;
  margin: auto;
  vertical-align: middle;
}

.seomun_btn {
  right: 0;
}

.hilton_btn {
  left: 0;
}
/****************contents****************/

.contents{
  display: none;
}

.project_wrap>div:first-child {
  margin-bottom: 150px;
}

}

  @media screen and (max-width: 540px) {
    .project_wrap>div:first-child {
    margin-bottom: 100px;
    }
  }
</style>
