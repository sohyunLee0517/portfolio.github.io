<template>
    <div class="logo" @click="moveToScroll('top')">
        <!-- <i></i> -->
        <img src="../assets/img/logo_dark.svg" class="logoImg">
    </div>
    <div class="menu">
        <div @click="moveToScroll('aboutMe')" :class="{'active' : scrollSection == 'aboutme'}">About me</div>
        <div @click="moveToScroll('skills')" :class="{'active' : scrollSection == 'skills'}">Skills</div>
        <div @click="moveToScroll('archiving')" :class="{'active' : scrollSection == 'archiving'}">Archiving</div>
        <div @click="moveToScroll('projects')" :class="{'active' : scrollSection == 'projects'}">Projects</div>
        <div @click="moveToScroll('career')" :class="{'active' : scrollSection == 'career'}">Career</div>
    </div>
</template>

<script>
export default {
  name: 'MainHeader',
  data(){
    return{
        scrollSection : ''
    }
  },
  mounted() {

      document.getElementsByTagName('main')[0].addEventListener('scroll', () => {
        let scrolltop = document.getElementsByTagName('main')[0].scrollTop;
        let maintop = document.getElementsByClassName('main-masthead')[0].scrollHeight - 100;
        let aboutmetop = maintop + document.getElementsByClassName('aboutMe')[0].scrollHeight - 100;
        let skillstop = aboutmetop + document.getElementsByClassName('skills')[0].scrollHeight - 100;
        let archivingtop = skillstop + document.getElementsByClassName('archiving')[0].scrollHeight - 100;
        let projectstop = archivingtop + document.getElementsByClassName('projects')[0].scrollHeight - 100;
        let careertop = projectstop + document.getElementsByClassName('career')[0].scrollHeight - 100;
        
        if(scrolltop < maintop){
            this.scrollSection = 'main'
        }else if(scrolltop > maintop && scrolltop < aboutmetop){
            this.scrollSection = 'aboutme'
        }else if(scrolltop > aboutmetop && scrolltop < skillstop){
            this.scrollSection = 'skills'
        } else if(scrolltop > skillstop && scrolltop < archivingtop){
            this.scrollSection = 'archiving'
        }else if(scrolltop > archivingtop && scrolltop < projectstop){
            this.scrollSection = 'projects'
        }else if(scrolltop > projectstop){
            this.scrollSection = 'career'
        }

      })
  },
  methods : {

      moveToScroll : (className, event) => {
        let el = document.getElementsByTagName('main')[0];

        if(className == 'top'){
            return el.scrollTop = 0
        }
        let nextEl = document.getElementsByClassName(className)[0].getBoundingClientRect().top;

        el.scrollTop = el.scrollTop + nextEl;

      }
  },
  watch : {
    scrollSection : (newVal, oldVal) => {
        console.log(newVal);
    }
  }

}
</script>