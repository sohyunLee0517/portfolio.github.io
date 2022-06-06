<template>
  <header :class="{'scrollMove' : isScrollMove}">
    <MainHeader />
  </header>
  <main>
    <Main />
    <footer>
      <MainFooter />
    </footer>
  </main>
</template>

<script>
import MainHeader from './components/header.vue'
import Main from './components/main.vue'
import MainFooter from './components/footer.vue'

export default {
  name: 'App',
  components: {
    MainHeader,
    Main,
    MainFooter
  },
  data : function(){
    return {
      isScrollMove : false
    }
  },
  mounted : function(){
    
    let self = this;
    
    let el = document.getElementsByTagName('main')[0];
    
    el.addEventListener('scroll', (evt)=>{
      this.headerScrollEvt(evt, self);
    });

  },
  methods : {
    headerScrollEvt : (e, self) => {
      e.preventDefault();

      let mastheadHeight = document.getElementsByClassName('main-masthead')[0].getBoundingClientRect().height - 50;

      if(e.target.scrollTop >= mastheadHeight){

        self.isScrollMove = true;
      
      }else{

        self.isScrollMove = false;

      }
    }
  }
}
</script>

<style scoped>
@import url(./assets/style.css);
</style>