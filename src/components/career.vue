<template>
  <div class="career">
    <div class="section-title">
        CAREER
    </div>
    <div class="section-wrap">
      <div class="section-box" v-for="list in careerList">
        <div class="section-box-title">{{list.title}}</div>
        <div class="section-box-sub-title">{{list.period}}</div>
        <img class="section-box-img" :src="list.img">
        <div class="section-box-item" v-html="list.desc"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Career',
  data (){
    return{
      careerList : [
        {
          title : 'pnp.so',
          period : '2021.03 ~ 2021.03',
          img : require('../assets/img/pnpso.png'),
          desc : 'pnp.so 에서 기존 html 페이지를 Vue.js로 변환하는 작업을 하였습니다.<br>칸반, 캘린더, 타임라인, 채팅, 웹문서 등 다양한 방식의 화면 개발을 경험했습니다.<br>시스템 특성상 모바일기기에서도 동일하게 보일 수 있도록, 반응형으로 제작하였습니다.'
        },
        {
          title : 'habil.so',
          period : '2021.04 ~ 2021.6',
          img : require('../assets/img/habilso.png'),
          desc : 'pnp.so의 단순버전으로, 기존 사용하던 Vue.js를 보다 더 효과적으로 사용할 수 있었습니다.<br>Vue.js로 프로젝트 셋팅(컴포넌트 구조, 파일 구조, 라우터)을 하였습니다.<br>Vuex를 본격적으로 front에 도입했으며, 전체 페이지 frontEnd를 담당하였습니다.'
        }
      ]
    }
  }
}
</script>
