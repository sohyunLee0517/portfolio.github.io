<template>
  <div class="main-masthead">
    <h4>프론트엔드 개발자</h4>
    <h1>이소현</h1>
    <div>안녕하세요.<br/>언제나 더 나은 품질과 UIUX를 위해 노력하는<br/> 보통의 새로운 FE 개발자 입니다.</div>
    <div class="main-under-icon"
    @click="scrollToNext"></div>
  </div>
  <section>
    <About/>
    <Skills/>
    <Archiving/>
    <Projects/>
    <Career/>
  </section>
</template>

<script>
import About from './about.vue'
import Archiving from './archiving.vue'
import Career from './career.vue'
import Projects from './projects.vue'
import Skills from './skills.vue'

export default {
  name: 'Main',
  components: {
    About,
    Archiving,
    Career,
    Projects,
    Skills
  },
  data : function(){
    return{

    }
  },
  methods : {
    scrollToNext : function(e){
      let el = document.getElementsByTagName('main')[0];

      let nextEl = document.getElementsByClassName('aboutMe')[0].getBoundingClientRect().top;

      el.scrollTop = el.scrollTop + nextEl;
    }
  }
}
</script>
