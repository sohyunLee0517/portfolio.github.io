<template>
  <div class="skills">
    <div class="section-title">
        SKILLS
    </div>
    <div class="section-wrap">
      <div class="section-box" v-for="list in skillList" :key="list.index">
        <div class="section-box-title">{{ list.title }}</div>
        <div class="section-box-item">
          <div class="section-box-item-img-group" v-show="list.title != 'sertificate'">
            <img
            v-for="item in list.list"
            :key="item.index"
            :src="item.img">
          </div>
          <div class="section-box-desc"
          :class="{'skillsNoImg' : list.title == 'sertificate'}" 
          v-html="list.desc"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  props: {
  },
  data : function(){
    return{
      skillList : [
        {
          title : 'FrontEnd',
          desc : '업무중에 css, html, javascript, vue.js를 사용하여 해당 툴들을 잘 사용할 수 있습니다.<br>vue.js는 프로젝트 구축하는 과정에서부터 시작하였습니다. vuex를 사용한 상태관리를 개발한 경험이 있으며, router를 활용한 페이지 전환을 개발한 경험이 있습니다. <br>개인 프로젝트로 react와 redux를 사용해본 경험이 있습니다.',
          list : [
            {
              title : 'Vue.js',
              img : require('../assets/img/vue.png')
            },
            {
              title : 'React',
              img : require('../assets/img/react.png')
            },
            {
              title : 'Java Script',
              img : require('../assets/img/js.png')
            },
            {
              title : 'CSS',
              img : require('../assets/img/css.png')
            },
            {
              title : 'HTML',
              img : require('../assets/img/html.png')
            }
          ]
        },{
          title : 'versiton control',
          desc : '깃을 사용하여 개인 프로젝트의 버전관리를 하였습니다.',
          list : [
            {
              title : 'github',
              img : require('../assets/img/github.png')
            },
          ]
        },{
          title : 'communication',
          desc : '업무중에 Figma와 XD를 사용하여 디자이너와 협업을 하였습니다.',
          list : [
            {
              title : 'figma',
              img : require('../assets/img/figma.png')
            },
            {
              title : 'adobeXD',
              img : require('../assets/img/adobeXD.png')
            },
          ]
        },{
          title : 'sertificate',
          desc : '2019.10.18 <b>웹디자인기능사</b>',
          list : [
            {
              title : '웹디자인기능사',
              img : ''
            }
          ]
        }
      ]
    }
  },
  methods :{
    setSrc : (src) => {
      return '../assets/img/' + src + '.png'
    }
  }
}
</script>
