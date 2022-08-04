<template>
    <section class="detail_wrap">
        <div class="detail">
            <h3>밀레니엄<em>힐튼 서울</em></h3>
            <img class="detail_img" src="../assets/hilton.png">
            <div class="contents">
                <p class="mb16">
                    <em>제작기간 :&nbsp;</em>
                    <em>2022.05 ~ 2022.06</em>
                </p>
                <p>참여율 : 30%</p>
                <div class="comment">
                    <span>
                        기존 사이트에서 부족했던 <em>디자인 요소 및</em><em>편의성을 개선하고,</em></span>
                    <span> 콘텐츠를 추가하여 <em>홈페이지를 새롭게 </em><em>제작했습니다.</em></span>
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
            <button class="btn" @click="gotoHilton()">WEB</button>
        </div>
    </section>
</template>

<script>

export default {
    name:"hiltonDetail",
    methods: {
      gotoHilton: function(){
      window.open("https://hiltonseoulfinal.herokuapp.com/", "_blank");
    }, 
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