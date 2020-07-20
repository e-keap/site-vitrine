<template>
  <footer class="footer px-4">
    <div class="row align-items-center justify-content-lg-between">
      <div class="plan">
        <h3>Plan du site</h3>
        <a href="#home">E.keap</a>
        <a href="#ekeap">Qui sommes nous ?</a>
        <a href="#equipe">Notre équipe</a>
        <a href="#application">Notre application</a>
      </div>
      <div class="lol">
        <h5>Réalisé dans le cadre d'un projet universitaire</h5>
      </div>
      <div class="team">
        <h3>Membres de l'équipe</h3>
        <a href="#home">COATRIEUX Anton </a>
        <a href="#home">GRIMAUD Estelle</a>
        <a href="#home">RIOU Kevin</a>
        <a href="#home">POIRIER Annais</a>
        <a href="#home">BLOUIN Pierre</a>
      </div>
    </div>
    <div class="row align-items-center justify-content-lg-between">
      <div class="col-lg-6">
        <div class="copyright text-center text-lg-left text-muted">
          © {{year}} <a href="#home" class="font-weight-bold ml-1">E.keap</a>
        </div>
      </div>
      <div class="col-lg-6">
        <ul class="nav nav-footer justify-content-center justify-content-lg-end">
          <li class="nav-item">
            Made with love by <a href="#home">E.keap</a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>

<style lang="scss" scoped>
  .plan{
    padding: 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;

    a{
      position: relative;
      margin: 0 20px;
      color: darkgrey;
      font-size: 12px;

      &:hover{
        &::before{
          content: '';
          position: absolute;
          width: 4px;
          height: 4px;
          background-color: #8150A0;
          top: calc(50% - 2px);
          left: -10px;
          border-radius: 50%;
        }
        &::after{
          content: '';
          position: absolute;
          width: 40px;
          height: 4px;
          background-color: #8150A0;
          top: calc(50% - 2px);
          right: -50px;
          border-radius: 4px;
        }
      }
    }
  }
  .team{
    padding: 30px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-end;

    a{
      position: relative;
      margin: 0 20px;
      color: darkgrey;
      font-size: 12px;

      &:hover{
        &::before{
          content: '';
          position: absolute;
          width: 40px;
          height: 4px;
          background-color: #8150A0;
          top: calc(50% - 2px);
          left: -50px;
          border-radius: 4px;
        }
        &::after{
          content: '';
          position: absolute;
          width: 4px;
          height: 4px;
          background-color: #8150A0;
          top: calc(50% - 2px);
          right: -10px;
          border-radius: 4px;
        }
      }
    }
  }
  .lol{
    padding: 30px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    height: 200px;
  }
</style>