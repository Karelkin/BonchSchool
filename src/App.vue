<template>
  <!-- <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div> -->
  <div>
    <app-header></app-header>
    <school></school>
    <study></study>
    <schedule></schedule>
    <results></results>
    <courses></courses>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader'
import School from '@/components/School'
import Study from '@/components/Study'
import Schedule from '@/components/Schedule'
import Results from '@/components/Results'
import Courses from '@/components/Courses'

export default{
  components: {
    AppHeader,
    School,
    Study,
    Schedule,
    Results,
    Courses
  }
}
</script>

<style lang="scss">
*{
  font-family: 'Avenir Next Cyr Regular', sans-serif;
  color: #48545C;
  line-height: 1;
}
.container{
  padding: 0;
  margin: 0 auto;
  max-width: 1350px;
}
.row{
  margin-left: 0;
  margin-right: 0;
}

</style>
