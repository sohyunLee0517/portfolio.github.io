<template>
  <div class="archiving">
    <div class="section-title">
        ARCHIVING
    </div>
    <div class="section-wrap">
      <div class="section-box motion" v-for="list in archiveList" @click="moveTo(list.url)">
        <div class="section-box-title">{{list.title}}</div>
        <img class="section-box-img-icon" :src="list.img" v-if="list.img != null && list.img != undefined">
        <div class="section-box-item" v-html="list.desc"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Archiving',
  data (){
    return{
      archiveList : [
        {
          title : 'github',
          img : require('../assets/img/github.png'),
          desc : '소스 코드 저장소 입니다.<br>제작하고 진행했던 프로젝트들과 흔적들이 남아있습니다.',
          url : 'https://github.com/sohyunLee0517'
        },
        {
          title : 'velog',
          img : require('../assets/img/velog.png'),
          desc : '공부와 알게된 지식 공유 블로그입니다.<br>공부를하며 깨달은 것들, 제가 작업하며 더 배운 것들에 대해 공유하기 위해 기록해 둔 블로그 입니다.',
          url : 'https://velog.io/@nonlyito'
        }
      ]
    }
  },
  methods : {
    moveTo : (url) => {
      window.open(url, '_blank');
    }
  }
}
</script>
