<template>
  <section class="intro_wrap">
    <div class="background"></div>
    <div class="hello">
      <div class="hellotext">
        <span class="hellotext01">H</span>
        <span class="hellotext02">E</span>
        <span class="hellotext03">L</span>
        <span class="hellotext04">L</span>
        <span class="hellotext05">O</span>
      </div>
      <div class="circle hellotext06"></div>
    </div>
    <div class="name">
        <span class="fadeup1">"</span>
        <span class="fadeup2">I’m</span>
        <span class="fadeup3">Front-end Developer</span>
        <span class="fadeup4">Hyunmin</span>
        <span class="fadeup5">"</span>
    </div>
  </section>
</template>

<script>

export default {
  name: 'intro-page',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.intro_wrap {
  width: 100%;
  height: 100vh;
  position: relative;
}

.background {
  width: 100%;
  height: 100%;
  background-color: #FFE033;
  position: absolute;
  left: -50%;
}

.hello {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  align-items: flex-end;
}

.hellotext {
  font-size: 250px;
  line-height: 0.4;
  font-family: 'Lalezar', cursive;
}

.circle {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #FFE033;
}

/**애니메이션1 hello fadein**/

.hellotext01 {
  opacity: 0;
  animation: animation01 2s ease-in 0.3s forwards;
}
.hellotext02 {
  opacity: 0;
  animation: animation01 2s ease-in 0.4s forwards;
}
.hellotext03 {
  opacity: 0;
  animation: animation01 2s ease-in 0.5s forwards;
}
.hellotext04 {
  opacity: 0;
  animation: animation01 2s ease-in 0.6s forwards;
}
.hellotext05 {
  opacity: 0;
  animation: animation01 2s ease-in 0.7s forwards;
}

.hellotext06 {
  opacity: 0;
  animation: animation01 2s ease-in 0.8s forwards, animation03 1.5s 2s ease-in forwards;
}

@keyframes animation01{
  from {
    opacity: 0;
  }
  to{
    opacity: 1;
  }
}

/**애니메이션2 배경 움직임**/

.background {
  animation: animation02 1s 2s ease-in-out forwards;
}


@keyframes animation02{
  from {
    left: -50%;
  }
  to{
    left: 0;
  }
}

/**애니메이션3 원형점 색변경**/

@keyframes animation03{
  from {
    background-color: #FFE033;
  }
  to{
    background-color: #fff;
  }
}

/**애니메이션4 hello 텍스트 이동**/

.hello {
  animation: animation04 2s 3.5s ease-in-out forwards;
}

@keyframes animation04{
  from {
    left: 50%;
  }
  to{
    left: 25%;
  }
}

/**애니메이션5 **/

.name{
  width: 50%;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 0;
  text-align: center;
  font-family: 'Lalezar', cursive;
}

.name>span {
  font-size: 58px;
  display: block;
  opacity: 0;
}

.fadeup1 {
  animation: animation05 2s 4s forwards;
}

.fadeup2 {
  animation: animation05 2s 4.5s forwards;
}

.fadeup3 {
  animation: animation05 2s 5s forwards;
}

.fadeup4 {
  color: #fff;
  animation: animation05 2s 5.5s forwards;
}

.fadeup5 {
  animation: animation05 2s 6s forwards;
}

@keyframes animation05{
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }
  to{
    opacity: 1;
    transform: translateZ(0);
  }
}

@media screen and (max-width: 1440px) {

.name{
  width: 70%;}

@keyframes animation04{
  from {
    left: 50%;
  }
  to{
    left: 0;
  }
}

}



@media screen and (max-width: 1000px) {

  .background {
  width: 100%;
  height: 100%;
  background-color: #FFE033;
  position: absolute;
  left: 0;
  animation:none;
}


.hello {
  left: 50%;
  transform: translate(-50%, -50%);
}

@keyframes animation04{
  from {
    left: 50%;
  }
  to{
    left: -150%;
  }
}

.circle {
  background-color: #FFF;
}

.hellotext06 {
  animation: animation01 2s ease-in 0.8s forwards, none;
}

@keyframes animation04{
  from {
    left: 50%;
  }
  to{
    left: -250%;
  }
}

.name{
  width: 100%;
}

  }
@media screen and (max-width: 768px) {

  .hello {
  left: 0;
  transform: translate(0, -50%);
}


@keyframes animation04{
  from {
    left: 0;
  }
  to{
    left: -300%;
  }
}

}

</style>
