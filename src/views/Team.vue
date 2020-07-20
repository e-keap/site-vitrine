<template>
  <div class="team">
    <div class="row team-list">
      <div class="col-lg-12 team-member" v-for="(member,i) in team" :key="i">
        <div class="img-container">
          <img :src="member.photo" :alt="'Photo de '+member.name"/>
        </div>
        <div class="right-info">
          <h3>{{ member.name }}</h3>
          <h4>{{ member.role }}</h4>
          <p>{{ member.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        team: [
          {
            name: 'Annaïs POIRIER',
            photo: '/img/team/Annais.png',
            role: 'Community Manager',
            description: 'Petite description'
          },
          {
            name: 'Pierre BLOUIN',
            photo: '/img/team/Pierre.PNG',
            role: 'Graphiste',
            description: 'Petite description'
          },
          {
            name: 'Estelle GRIMAUD',
            photo: '/img/team/Estelle.PNG',
            role: 'Chargée Marketing',
            description: 'Petite description'
          },
          {
            name: 'Anton COATRIEUX',
            photo: '/img/team/Anton.png',
            role: 'Développeur Back',
            description: 'Petite description'
          },
          {
            name: 'Kévin RIOU',
            photo: '/img/team/Kevin.png',
            role: 'Développeur Front',
            description: 'Jeune développeur, axé sur la création de site web, j\'y prend du plaisir. I am Groot'
          }
        ]
      }
    },
  }
</script>

<style lang="scss" scoped>
  .team-list{
    justify-content: center;
    align-items: center;

    .team-member{
      margin: 25px;
      width: 400px;
      min-width: 400px;
      max-width: 600px;

      display:flex;
      flex-wrap: nowrap;
      align-items: center;
      justify-content: center;

      .img-container{
        background: linear-gradient(45deg, #32325d 0%, #F17851 100%);
        border-radius: 50%;
        height: 150px;
        width: 150px;
        margin: 50px 50px 0 0;
        display: flex;
        justify-content: center;
        align-items: center;

        img{
          transform: scale(1.2);
          margin: 0 0 50px 50px;
          height: 150px;
        }
      }
      

      .right-info{
        display: block;
      }
    }
  }
</style>