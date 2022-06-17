<template>
  <div class="career">
    <div class="section-title">
        CAREER
    </div>
    <div class="section-wrap">
      <div class="section-box" v-for="list in careerList">
        <div class="section-box-title">{{list.title}}</div>
        <img class="section-box-img" :src="list.img">
        <div class="section-box-item" v-text="list.desc"></div>
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
          img : require('../assets/img/pnpso.png'),
          desc : 'pnp.so 에서 기존 html 페이지를 vue로 변환하는 작업을 하였습니다. 또한, 칸반, 캘린더, 타임라인, 채팅, 웹문서 등 다양한 방식의 화면 개발을 경험했습니다.'
        },
        {
          title : 'habil.so',
          img : require('../assets/img/habilso.png'),
          desc : 'pnp.so의 단순버전으로, 기존 사용하던 vue를 보다 더 효과적으로 사용할 수 있었습니다. vue로 프로젝트 셋팅부터 시작하여 개발하였습니다.vuex를 본격적으로 front에 도입했으며, '
        }
      ]
    }
  }
}
</script>
