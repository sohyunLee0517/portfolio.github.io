<template>
  <div class="skills">
    <div class="section-title">
        SKILLS
    </div>
    <div class="section-wrap">
      <div class="section-box" v-for="list in skillList" :key="list.index">
        <div class="section-box-title">{{ list.title }}</div>
        <div class="section-box-item"
        v-for="item in list.list"
        :key="item.index">
          <div class="section-box-item-img" :class="item.img"></div>
          <div>
            <div>{{item.title}}</div>
            <div>{{item.proficiency}}</div>
          </div>
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
          list : [
            {
              title : 'Java Script',
              img : 'js',
              proficiency : '7'
            },
            {
              title : 'Vue.js',
              img : 'vue',
              proficiency : '8'
            },
            {
              title : 'React',
              img : 'react',
              proficiency : '5'
            },
            {
              title : 'CSS',
              img : 'css',
              proficiency : '5'
            },
            {
              title : 'HTML',
              img : 'html',
              proficiency : '5'
            }
          ]
        },{
          title : 'versiton control',
          list : [
            {
              title : 'github',
              img : 'github',
              proficiency : '5'
            },
          ]
        },{
          title : 'communication',
          list : [
            {
              title : 'figma',
              img : 'figma',
              proficiency : '7'
            },
          ]
        },{
          title : 'sertificate',
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
