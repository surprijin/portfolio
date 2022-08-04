<template>
  <section class="w1200">
    <h1>Skills</h1>
    <article>
      <ul>
        <li>
          <div class="skill_title">HTML</div>
          <div class="skill_level">
            <span class="w70 skills html">
              <em>70%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">CSS</div>
          <div class="skill_level">
            <span class="w75 skills css">
              <em>75%</em>            
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">Javascript</div>
          <div class="skill_level">
            <span class="w50 skills js">
              <em>50%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">jQuery</div>
          <div class="skill_level">
            <span class="w50 skills jquery">
              <em>50%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">Vue.js</div>
          <div class="skill_level">
            <span class="w40 skills vue">
              <em>40%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">Node.js</div>
          <div class="skill_level">
            <span class="w30 skills node">
              <em>30%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">Mysql</div>
          <div class="skill_level">
            <span class="w40 skills mysql">
              <em>40%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">heroku</div>
          <div class="skill_level">
            <span class="w40 skills heroku">
              <em>40%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">github</div>
          <div class="skill_level">
            <span class="w40 skills github">
              <em>40%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">figma</div>
          <div class="skill_level">
            <span class="w65 skills figma">
              <em>65%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">Photoshop</div>
          <div class="skill_level">
            <span class="w70 skills photoshop">
              <em>70%</em>
            </span>
          </div>
        </li>
        <li>
          <div class="skill_title">illustrator</div>
          <div class="skill_level">
            <span class="w60 skills ai">
              <em>60%</em>
            </span>
          </div>
        </li>
      </ul>
    </article>
  </section>
</template>

<script>
export default {
  name: 'skill-page',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.skills {
  display: none;
}

ul>li {
  display: flex;
  font-size: 19px;
}

ul>li:not(:last-child) {
  margin-bottom: 16px;
}

.skill_title {
  width: 120px;
  font-weight: 600;
  
}

.skill_level {
  width: calc(100% - 120px);
  background-color: #e9e9e9;
  border-radius: 3px;
  position: relative;
}

.skill_level>span{
  position: relative;
  height: 100%;
  top: 0;
  left: 0;
  border-radius: 3px;
  opacity: 0.7;
}

.skill_level>.html {
 background-color: #f16529;
}
.skill_level>.css {
 background-color: #29a9df;
}
.skill_level>.js {
 background-color: #f0db4f;
}
.skill_level>.jquery {
 background-color: #0868ac;
}
.skill_level>.vue {
 background-color: #4eb282;
}
.skill_level>.node {
 background-color: #2e7d32;
}
.skill_level>.mysql {
 background-color: #1a7196;
}
.skill_level>.github {
 background-color: #171516;
}
.skill_level>.heroku {
 background-color: #3d347b;
}
.skill_level>.figma {
 background-color: #ff7262;
}
.skill_level>.photoshop {
 background-color: #31a8ff;
}
.skill_level>.ai {
 background-color: #ff9b00;
}

.skill_level>.w75{
  width: 75%;
  animation: graph75 2s ease-in;
}

@keyframes graph75 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 75%;}
}

.skill_level>.w65 {
  width: 65%;
  animation: graph65 2s ease-in;
}

@keyframes graph65 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 65%;}
}


.skill_level>.w70{
  width: 70%;
  animation: graph70 2s ease-in;
}

@keyframes graph70 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 70%;}
}

.skill_level>.w60{
  width: 60%;
  animation: graph60 2s ease-in;
}

@keyframes graph60 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 60%;}
}

.skill_level>.w50{
  width: 50%;
  animation: graph50 2s ease-in;
}

@keyframes graph50 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 50%;}
}

.skill_level>.w40{
  width: 40%;
  animation: graph40 2s ease-in;
}

@keyframes graph40 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 40%;}
}

.skill_level>.w30{
  width: 30%;
  animation: graph30 2s ease-in;
}

@keyframes graph30 {
  0% {width: 0; color: grba(255,255,255,0);}
  50% {color:grba(255,255,255,10)}
  100% {width: 30%;}
}

.skill_level em {
  display: block;
  width: 100%;
  padding-right: 10px;
  box-sizing: border-box;
  text-align: right;
  color: #fff;
}

@media screen and (max-width: 768px) {
ul>li {
  font-size: 16px;
}

.skill_level {
  width: calc(100% - 100px);}

.skill_title {
  width: 100px;
}
}
</style>