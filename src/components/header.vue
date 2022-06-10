<template>
    <div class="logo" @click="moveToScroll('top')">
        YSH's Portfolio
    </div>
    <div class="menu">
        <div @click="moveToScroll('aboutMe')">About me</div>
        <div @click="moveToScroll('skills')">Skills</div>
        <div @click="moveToScroll('archiving')">Archiving</div>
        <div @click="moveToScroll('projects')">Projects</div>
        <div @click="moveToScroll('career')">Career</div>
    </div>
</template>

<script>
export default {
  name: 'MainHeader',
  props: {
  },
  methods : {
      moveToScroll : (id, event) => {
        let el = document.getElementsByTagName('main')[0];

        if(id == 'top'){
            return el.scrollTop = 0
        }
        let nextEl = document.getElementsByClassName(id)[0].getBoundingClientRect().top;

        el.scrollTop = el.scrollTop + nextEl;

      }
  }
}
</script>