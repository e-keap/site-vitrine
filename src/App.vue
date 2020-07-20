<template>
  <div id="app">
    <notifications></notifications>
    <Title titre="Qui sommes nous ?"/>
    <Dashboard />
    <!-- <router-view/> -->
    <Title titre="Notre équipe"/>
    <Team />
    <Title titre="Notre application"/>
    <Screens />
  </div>
</template>

<script>
import Title from './components/Title'

import Team from './views/Team'
import Dashboard from './views/Dashboard'
import Screens from './views/Screens'

export default {
  components: {
    Title,
    Team,
    Dashboard,
    Screens
  },
}
</script>

<style lang="scss">
  html {
    overflow-x: hidden
  }
</style>
