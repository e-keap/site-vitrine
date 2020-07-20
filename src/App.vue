<template>
  <div id="app">
    <notifications></notifications>
    <Head />
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
import Head from './views/Head'
import Dashboard from './views/Dashboard'
import Screens from './views/Screens'
import Chiffres from './views/Chiffres'

export default {
  components: {
    Title,
    Team,
    Dashboard,
    Screens,
    Chiffres,
    Head
  },
}
</script>

<style lang="scss">
  html {
    overflow-x: hidden
  }
</style>
