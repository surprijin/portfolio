<template>
  <topHeader></topHeader>
  <intro id="intro"></intro>
  <about id="about"></about>
  <skills id="skills"></skills>
  <project id="project"></project>
  <webclone id="cloning"></webclone>
  <contact id="contact"></contact>
  <div class="topbtn" v-on:click="toTop" v-show="scY">TOP</div>
</template>

<script>
 import intro from './components/intro.vue'
 import about from './components/about.vue'
 import skills from './components/skills.vue'
 import project from './components/project.vue'
 import webclone from './components/webclone.vue'
 import contact from './components/contact.vue'
 import topHeader from './components/header.vue'

 export default {
  name:'App',
  data() {
      return {
        scTimer: 0,
        scY: 0,
      }
    },
    mounted() {

      window.addEventListener('scroll', this.handleScroll);
      
    },
  methods: {
    handleScroll: function () {
        if (this.scTimer) return;
        this.scTimer = setTimeout(() => {
          this.scY = window.scrollY;
          clearTimeout(this.scTimer);
          this.scTimer = 0;
        }, 100);
    },
    toTop: function () {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
  },
  components: {
    intro,
    about,
    skills,
    project,
    webclone,
    contact,
    topHeader
  }
 }
</script>

<style scoped>


/*****************top버튼*****************/

.topbtn {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  border: 1px solid #FFA619;
  background-color: #fff;
  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
  color: #FFA619;
  font-weight: 600;
  cursor: pointer;
  position: fixed;
  bottom: 20px;
  right: 20px;
  text-align: center;
  line-height: 50px;
}

.topbtn:hover {
  background-color: #FFA619;
  color: #fff;
}

</style>

