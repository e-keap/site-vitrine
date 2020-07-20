<template>
  <div class="links">
    <a href="#home">E.keap</a>
    <a href="#ekeap">Qui sommes nous ?</a>
    <a href="#equipe">Notre équipe</a>
    <a href="#application">Notre application</a>
  </div>
</template>

<style lang="scss" scoped>
  .links{
    z-index: 500;
    top: 0;
    left: 0;
    padding: 30px;
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;

    a{
      position: relative;
      margin: 0 20px;
      color: white;
      font-size: 18px;

      &:hover{
        &::before{
          content: '';
          position: absolute;
          width: 100%;
          height: 3px;
          background-color: #8150A0;
          bottom: -3px;
          left: 0;
        }
      }
    }
  }
</style>