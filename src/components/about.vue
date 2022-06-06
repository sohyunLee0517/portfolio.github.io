<template>
  <div class="aboutMe">
    <div class="section-title">
        ABOUT ME
    </div>
    <div class="section-wrap">
      <div class="section-box" 
      v-for="list in myInfoList"
      :key="list.index">
        <div>
          <div class="section-box-icon">
            icon
            <img :src="list.icon">
          </div>
          <div class="section-cts">
            <div class="section-cts-title">{{ list.title }}</div>
            <div class="section-cts-text">{{ list.txt }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
  data: function(){
    return {
      myInfoList : [
        {
          icon : '',
          title : '이름',
          txt : '이소현'
        },
        {
          icon : '',
          title : '생년월일',
          txt : '95.01.13'
        },
        {
          icon : '',
          title : '주소지',
          txt : '경기도 김포시'
        },
        {
          icon : '',
          title : '연락처',
          txt : '010'
        },
        {
          icon : '',
          title : '이메일',
          txt : 'nonlyito@gmail.com'
        },
        {
          icon : '',
          title : '학력',
          txt : '방송통신대학교(컴퓨터과학과)'
        }
      ]
    }
  }
}
</script>
