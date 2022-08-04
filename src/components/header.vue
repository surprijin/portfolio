<template>
 <nav class="main_nav">
    <div>
      <div>
        <h1>
          <div class="logo"></div>
        </h1>
        <ul class="tabList">
          <li v-on:click="gotointro" class="list active">INTRO</li>
          <li v-on:click="gotoabout" class="list">ABOUT</li>
          <li v-on:click="gotoskill" class="list">SKILLS</li>
          <li v-on:click="gotoproject" class="list">PROJECT</li>
          <li v-on:click="gotocloning" class="list">CLONING</li>
          <li v-on:click="gotocontact" class="list">CONTACT</li>
        </ul>
      <div class="m_tab" @click="mNav = true"></div>
      </div>
    </div>
  </nav>
  <div class="mNav" v-if="mNav == true" @click="mNav = false">
    <div class="mNavTop">
      <div class="mLogo"></div>
      <div class="closebtn"></div>
    </div>
    <h3>HYUNMIN’s Portfolio</h3>
    <ul class="mtabList">
      <li v-on:click="gotointro" class="mlist">INTRO</li>
      <li v-on:click="gotoabout" class="mlist">ABOUT</li>
      <li v-on:click="gotoskill" class="mlist">SKILLS</li>
      <li v-on:click="gotoproject" class="mlist">PROJECT</li>
      <li v-on:click="gotocloning" class="mlist">CLONING</li>
      <li v-on:click="gotocontact" class="mlist">CONTACT</li>
    </ul>
    <div class="giticon" onclick="window.open('https://github.com/surprijin');"></div>
  </div>
  <nav class="sidemenu">
      <ul>
        <li class="sdlist" v-on:click="gotointro">
          <em>INTRO</em>
        </li>
        <li class="sdlist" v-on:click="gotoabout">
          <em>ABOUT</em>
        </li>
        <li class="sdlist" v-on:click="gotoskill">
          <em>SKILLS</em>
        </li>
        <li class="sdlist" v-on:click="gotoproject">
          <em>PROJECT</em>
        </li>
        <li class="sdlist" v-on:click="gotocloning">
          <em>CLONING</em>
        </li>
        <li class="sdlist" v-on:click="gotocontact">
          <em>CONTACT</em>
        </li>
      </ul>
    </nav>

</template>

<script>
export default {
    name: "topHeader",
    data() {
      return {
        mNav : false,
      }
    },
     methods: {
    //클릭시 해당 페이지 이동 스크립트 
    gotointro() {
      const intro = document.getElementById('intro');
      if(intro) {
        intro.scrollIntoView({behavior:'smooth'})
      }
    },
    gotoabout() {
      const about = document.getElementById('about');
      if(about){
        about.scrollIntoView({behavior:'smooth'})
      }
    },
    gotoskill() {
      const skill = document.getElementById('skills');
      if(skill){
        skill.scrollIntoView({behavior:'smooth'})
      }
    },
    gotoproject() {
      const project = document.getElementById('project');
      if(project){
        project.scrollIntoView({behavior:'smooth'})
      }
    },
    gotocloning() {
      const cloning = document.getElementById('cloning');
      if(cloning){
        cloning.scrollIntoView({behavior:'smooth'})
      }
    },
    gotocontact() {
      const contact = document.getElementById('contact');
      if(contact) {
        contact.scrollIntoView({behavior:'smooth'})
      }
    },
  },
}
</script>

<style scoped>

.main_nav {
  width: 100%;
  height: 60px;
  background-color: #FFE033;
  padding: 10px 0;
  box-sizing: border-box;
  position: fixed;
  z-index: 89;
}

.main_nav>div {
  width:1440px;
  margin: auto;
}

.main_nav>div>div {
  display: flex;
  justify-content: space-between;
}

/*********************로고*************************/

.logo, .mLogo {
  width: 145px;
  height: 40px;
  background-image: url('../assets/logo.png');
  background-size: cover;
}

/*********************nav*************************/

.tabList {
  display: flex;
  align-items: flex-end;
}

.tabList>li {
  margin-left: 24px;
  font-weight: 700;
  cursor: pointer;
}

.tabList>li:hover {
  color: #fff;
}

/*********************모바일 탭**************************/

.m_tab {
  width: 30px;
  height: 30px;
  cursor: pointer;
  display: none;
  background-image: url('../assets/menu.svg');
  background-size: cover;
}


.active {
  color: #FFA619;
}

/*****************햄버거메뉴*****************/

.mNav {
  width: 100%;
  height: 100%;
  background-color: #FFF;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  text-align: center;
  display: none;
}

.mNavTop {
  width: 100%;
  height: 60px;
  padding: 0 30px;
  background-color: #FFE033;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.closebtn {
  width: 30px;
  height: 30px;
  background-image: url('../assets/close.svg');
  background-size: cover;
}

.mNav>h3 {
  font-size: 33px;
  font-weight: 700;
  margin: 24px 0;
}

.mtabList>li {
  line-height: 60px;
  font-size: 19px;
  cursor: pointer;
}

.giticon {
  width: 60px;
  height: 60px;
  margin: 30px auto 0;
  background-image: url('../assets/git_logo.png');
  background-size: cover;
  cursor: pointer;
}

/*********************퀵메뉴**************************/

.sidemenu {
  position: fixed;
  top: 50%;
  right: 20px;
  transform: translate(0, -50%);
  display: none;
  z-index: 89;
}


.sidemenu>ul>li {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  margin: 10px 0;
  position: relative;
  text-align: right;
  cursor: pointer;
}

.sdlist {
  background-color: #e9e9e9;
}

.sdactive {
  animation: changeColor 0.3s ease-in-out forwards;
}

@keyframes changeColor {
  from {
    background-color: #e9e9e9;
  }
  to {
    background-color: #FFA619;
  }
}

.sidemenu>ul>li:hover {
  background-color: #FFA619;
  transform: scale(1.2);
  transition: all 0.2s ease-in;
}

.sidemenu>ul>li:hover em {
  line-height: 15px;
  font-size: 14px;
  animation: fadein 1s;
}

@keyframes fadein {
    from {
        opacity:0;
    }
    to {
        opacity:1;
    }
}

.sidemenu>ul>li>em {
    text-align: right;
    position: absolute;
    right: 25px;
    font-weight: 600;
    color: #494949;
    opacity: 0;
}

@media screen and (max-width: 1440px) {
    .main_nav>div {
        width: 100%;
        padding: 0 30px;
        box-sizing: border-box;
    }

    .sidemenu, .sdlist, .sdactive {
      display: none;
    }
  }


  @media screen and (max-width: 768px) {

    .main_nav>div>div {
      align-items: center;
    }

    .mobileMenu, .tabList  {
      display: none;
    }

    .m_tab, .mNav{
      display: block;
    }
  }

</style>