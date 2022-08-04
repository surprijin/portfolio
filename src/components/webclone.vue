<template>
  <section class="w1200">
    <h1>web clone</h1>
    <article>
      <ul class="cloning_wrap">
        <li>
          <img src="../assets/garden_main.png">
          <div class="cloning_contents">
            <h4 class="mb16">싱그러운 집</h4>
            <p class="mb16">
              <span>제작기간:</span>
              <span>2022.00.00 ~ 2022.00.00</span>
            </p>
            <div class="icon_wrap mb16">
              <p class="mb16">Language & Tool</p>
              <div class="cloning_icon">
                <img src="../assets/html.png">
                <img src="../assets/css.png">
                <img src="../assets/js.png">
                <img src="../assets/jquery.png">
              </div>
            </div>
            <p>메인 페이지 / 커뮤니티 페이지 / 반응형 구현</p>
          </div>
        </li>
        <li>
          <img src="../assets/daejeon_main.png">
          <div class="cloning_contents">
            <h4 class="mb16">대전문화재단</h4>
            <p class="mb16">
              <span>제작기간:</span>
              <span>2022.00.00 ~ 2022.00.00</span>
            </p>
            <div class="icon_wrap mb16">
              <p class="mb16">Language & Tool</p>
              <div class="cloning_icon">
                <img src="../assets/html.png">
                <img src="../assets/css.png">
                <img src="../assets/js.png">
                <img src="../assets/jquery.png">
              </div>
            </div>
            <p>메인 페이지 / 대전무형문화재전수회관 / 반응형 구현</p>
          </div>
        </li>
        <li>
          <img src="../assets/pollexzone_main.png">
          <div class="cloning_contents">
            <h4 class="mb16">Pollex zone</h4>
            <p class="mb16">
              <span>제작기간:</span>
              <span>2022.00.00 ~ 2022.00.00</span>
            </p>
            <div class="icon_wrap mb16">
              <p class="mb16">Language & Tool</p>
              <div class="cloning_icon">
                <img src="../assets/html.png">
                <img src="../assets/css.png">
                <img src="../assets/js.png">
                <img src="../assets/jquery.png">
              </div>
            </div>
            <p>메인 페이지 / 소개 페이지 / 반응형 구현</p>
          </div>
        </li>
      </ul>
    </article>
  </section>
</template>

<script>
export default {
  name: 'webclone-page',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.cloning_wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.cloning_wrap>li {
  width: 32%;
  padding: 20px 10px 0;
  box-sizing: border-box;
  border: 1px solid #e9e9e9;
  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
  cursor: pointer;
}


.cloning_wrap>li>img {
  width: 100%;
  border: 1px solid #e9e9e9;
}

.cloning_contents {
  width: 100%;
  padding: 30px 0 40px;
  box-sizing: border-box;
  text-align: center;
}

.icon_wrap>p, .cloning_contents>h4 {
  font-weight: 600;
}

.cloning_contents>h4 {
  font-size: 24px;
  font-weight: 700;
}

.cloning_icon>img {
  width: 60px;
  height: 60px;
}

.cloning_icon>img:not(:last-child){
  margin-right: 24px;
}


@media screen and (max-width: 1200px) {

  .cloning_wrap>li {
    width: 100%;
  }

  .cloning_wrap>li:not(:last-child){
    margin-bottom: 30px;
  }
}

@media screen and (max-width: 768px) {

  .cloning_icon>img {
  width: 40px;
  height: 40px;
}

}

@media (hover:hover) and (min-width:769px) {
  .cloning_wrap>li:hover {
  border: 2px solid #FFE033;
}

}
</style>
