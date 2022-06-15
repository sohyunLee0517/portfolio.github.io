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
            <div class="section-box-item-img"
            v-for="item in list.list"
            :key="item.index"
            :class="item.img"></div>
          </div>
          <div class="section-box-desc"
          :class="{'skillsNoImg' : list.title != 'sertificate'}" 
          v-text="list.desc"></div>
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
          desc : '저는 프론트엔드를 하고 있습니다요',
          list : [
            {
              title : 'Java Script',
              img : 'js'
            },
            {
              title : 'Vue.js',
              img : 'vue'
            },
            {
              title : 'React',
              img : 'react'
            },
            {
              title : 'CSS',
              img : 'css'
            },
            {
              title : 'HTML',
              img : 'html'
            }
          ],
          desc : ''
        },{
          title : 'versiton control',
          desc : '',
          list : [
            {
              title : 'github',
              img : 'github'
            },
          ],
          desc : ''
        },{
          title : 'communication',
          list : [
            {
              title : 'figma',
              img : 'figma'
            },
          ],
          desc : ''
        },{
          title : 'sertificate',
          list : [
            {
              title : '웹디자인기능사',
              img : ''
            }
          ],
          desc : '웹디자인기능사를 땄습니다.'
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
