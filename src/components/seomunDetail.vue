<template>
    <section class="detail_wrap">
        <div class="detail">
            <h3>서문시장야시장</h3>
            <img class="detail_img" src="../assets/seomun.png">
            <div class="contents">
                <p class="mb16">
                    <em>제작기간 :&nbsp;</em>
                    <em>2022.03 ~ 2022.07</em>
                </p>
                <p>참여율 : 100%</p>
                <div class="comment">
                    <span>기존 사이트에서 <em>부족했던 색감과</em><em>디자인의 통일성을 개선하고,</em></span>
                    <span>사용자의 편의성을 고려하여</span>
                    <span>메인, 소개, 공지사항 페이지를 <em>새롭게 제작했습니다.</em></span>
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
            </div>
            <button class="btn" @click="gotoSeomun()">WEB</button>
        </div>
    </section>
</template>

<script>

export default {
    name:"seomunDetail",
    methods: {
      gotoSeomun: function(){
      window.open("https://seomunmarket.herokuapp.com/", "_blank");
    }
    },
}
</script>

<style scoped>

.detail_wrap {
    position: fixed;
    padding: 30px;
    box-sizing: border-box;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 99;
}

.detail {
    position: relative;
    top: 50%;
    transform: translate(0, -50%);
    width: 100%;
    height: 100%;
    background-color: #fff;
    border-radius: 10px;
    margin: auto;
    padding: 20px;
    box-sizing: border-box;
    overflow-y: scroll;
    text-align: center;
}

.detail {
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.detail::-webkit-scrollbar {
    display: none;
}

h3 {
    font-size: 33px;
    font-weight: 600;
}

.detail_img {
    width: 80%;
    margin: 50px auto;
}

/**********컨텐츠*************/

.contents {
    width: 100%;
    text-align: center;
}

p, h5 {
    font-size: 19px;
    font-weight: 600;
}

.comment {
    margin: 30px 0;
}

.comment>span  {
    display: block;
}

.languages_icon {
    width: 100%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 16px;
}

.languages_icon>img {
    width: 60px;
    height: 60px;
}

.languages_icon>img:not(:last-child){
    margin-right: 24px;
}

.btn {
    margin-top: 30px;
}

em {
    display: inline-block;
}

  @media screen and (max-width: 540px) {

    .languages_icon {
        justify-content: space-between;
    }

    .languages_icon>img {
        width: 40px;
        height: 40px;
        margin-bottom: 10px;
    }

    .languages_icon>img:not(:last-child){
    margin-right: 0;
}

}

@media screen and (max-width: 420px) {

    h3 {
        font-size: 24px;
    }

    p, h5 {
        font-size: 16px;
    }

    .detail_wrap {
        font-size: 14px;
    }

    .detail_img {
        width: 100%;
    }

}

</style>
