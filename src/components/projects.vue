<template>
  <div class="projects">
    <div class="section-title">
        PROJECTS
    </div>
    <div class="section-wrap">
      <div class="section-box" v-for="list in projectsList">
        <div class="section-box-title">{{list.title}}</div>
        <div class="section-box-sub-title">{{list.period}}</div>
        <img class="section-box-img" :src="list.img" v-if="list.img != null && list.img != undefined">
        <div class="section-box-item" v-html="list.desc"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data (){
    return{
      projectsList : [
        {
          title : '애자일성장플랫폼 ASP개발',
          period : '2019.11.25 ~ 2021.04',
          desc : '해당 프로젝트를 통해 사용자가 Agile scale up 을 경험할 수 있도록 UX.UI를 발전시키기 위해 프로젝트를 진행하였습니다.'
        }
      ]
    }
  }
}
</script>
