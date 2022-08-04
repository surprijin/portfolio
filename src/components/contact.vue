<template>
  <section>
    <div class="contact_wrap">
      <h1>Contact me</h1>
      <div class="contact_contents">
        <p class="resolve">
          <span>“끊임없는 노력으로 어제보다는 오늘, &nbsp;</span>
          <span>오늘보다는 내일이 더 나은 개발자가 되겠습니다.”</span>
        </p>
        <p class="email">surprijin@naver.com</p>
        <p class="phone">+82) 010 - 2038 - 0538</p>
        <div class="giticon"  @click="gotoGithub()">
          <div></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'contact-page',
  methods: {
    gotoGithub: function(){
      window.open("https://github.com/surprijin", "_blank");
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  section {
    width: 100%;
    background-color: #FFE033;
    margin-top: 100px;
  }

  .contact_wrap {
    padding: 70px 0;
    box-sizing: border-box;
  }

  .contact_contents{
    width: 1200px;
    margin: auto;
    text-align: center;
  }

  .resolve {
    margin: 50px 0;
    font-weight: 500;
  }

  .resolve>span {
    display: inline-block;
  }

  .email{
    margin-bottom: 16px;
  }

  .phone {
    margin-bottom: 30px;
  }

  .giticon {
    width:60px;
    height: 60px;
    margin: auto;
  }

  .giticon>div {
    width: 100%;
    height: 100%;
    background-image: url('../assets/git_logo.png');
    background-size: cover;
    cursor: pointer;
  }

  @media screen and (max-width: 1200px) {
    .contact_contents {
        width: 100%;
    }
  }

  @media screen and (max-width: 768px) {
    section {
      height: 100vh;
    }

    .contact_wrap{
      position: relative;
      top: 50%;
      transform: translate(0, -50%);
    }

    .resolve>span {
      display: block;
    }
  }

</style>
