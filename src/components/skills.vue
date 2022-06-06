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
          <img :src="item.src">
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
              img : '',
              proficiency : '7'
            },
            {
              title : 'Vue.js',
              img : '',
              proficiency : '8'
            },
            {
              title : 'React',
              img : '',
              proficiency : '5'
            },
            {
              title : 'CSS',
              img : '',
              proficiency : '5'
            },
            {
              title : 'HTML',
              img : '',
              proficiency : '5'
            }
          ]
        },{
          title : 'versiton control',
          list : [
            {
              title : 'git',
              img : ''
            },
            {
              title : 'github',
              img : ''
            },
          ]
        },{
          title : 'communication',
          list : [
            {
              title : 'figma',
              img : ''
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
  }
}
</script>
