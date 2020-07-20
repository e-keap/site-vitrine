<template>
  <div id="app">
    <notifications></notifications>
    <Title titre="Qui sommes nous ?"/>
    <Dashboard />
    <Chiffres />
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
import Chiffres from './views/Chiffres'

export default {
  components: {
    Title,
    Team,
    Dashboard,
    Screens,
    Chiffres
  },
}
</script>

<style lang="scss">
  html {
    overflow-x: hidden
  }
</style>
