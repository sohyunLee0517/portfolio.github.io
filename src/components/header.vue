<template>
    <div class="logo">
        YSH's Portfolio
    </div>
    <div class="menu">
        <div @click="moveMenu('about')">About me</div>
        <div @click="moveMenu('skills')">Skills</div>
        <div @click="moveMenu('archiving')">Archiving</div>
        <div @click="moveMenu('projects')">Projects</div>
        <div @click="moveMenu('career')">Career</div>
    </div>
</template>

<script>
export default {
  name: 'MainHeader',
  props: {
  }
}
</script>