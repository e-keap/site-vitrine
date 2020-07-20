<template>
  <div id="app">
    <!-- <notifications></notifications> -->
    <Menu />
    <Head id="home"/>
    <Title titre="Qui sommes nous ?" id="ekeap"/>
    <Dashboard />
    <Chiffres />
    <!-- <router-view/> -->
    <Title titre="Notre équipe" id="equipe"/>
    <Team />
    <Title titre="Notre application" id="application"/>
    <Screens />
    <content-footer />
  </div>
</template>

<script>
import Title from './components/Title'

import Team from './views/Team'
import Head from './views/Head'
import Dashboard from './views/Dashboard'
import Screens from './views/Screens'
import Chiffres from './views/Chiffres'
import Menu from './views/Menu'

import ContentFooter from './layout/ContentFooter.vue';

export default {
  components: {
    Title,
    Team,
    Dashboard,
    Screens,
    Chiffres,
    Head,
    ContentFooter,
    Menu
  },
}
</script>

<style lang="scss">
  html {
    overflow-x: hidden;
    scroll-behavior: smooth;
  }
</style>
