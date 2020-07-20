<template>
    <div class="row chiffres">
      <div class="chiffre">
        <h1>
          <animated-number
            :value="12.5"
            :formatValue="formate"
            :duration="300"
          />
        </h1>
        <h2>Milliards/an</h2>
        <p class="desc">
          Tickets imprimés en france
        </p>
      </div>
      <div class="chiffre">
        <h1>
          <animated-number
            :value="110000"
            :formatValue="format"
            :duration="300"
          />
        </h1>
        <h2>kms/an (2.7 fois le tour de la terre)</h2>
        <p class="desc">
          De tickets imprimés par Auchan
        </p>
      </div>
      <div class="chiffre">
        <h1>
          <animated-number
            :value="5"
            :formatValue="format"
            :duration="300"
          />
        </h1>
        <h2>secondes</h2>
        <p class="desc">
          De durée de vie moyenne d'un ticket
        </p>
      </div>
      <div class="chiffre">
        <h1>
          <animated-number
            :value="10000"
            :formatValue="format"
            :duration="300"
          />
        </h1>
        <h2>rouleaux/an</h2>
        <p class="desc">
          Utilisés en moyenne par une grande surface
        </p>
      </div>
    </div>
</template>

<script>
  import AnimatedNumber from "animated-number-vue";

  export default {
    components: {
      AnimatedNumber,
    },
    data() {
      return {
        
      };
    },
    methods: {
      format(val){
        return `${val.toFixed(0)}`
      },
      formate(val){
        return `${val.toFixed(1)}`
      }
    },
    mounted() {
    }
  };
</script>

<style lang="scss" scoped>
  .chiffres{
    justify-content: center;
  }
  .chiffre{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 30px;

    h1{
      font-size: 65px;
      font-weight: bold;
      color: #8150A0;
      white-space: nowrap;
    }
    h2{
      white-space: nowrap;
      font-size: 12px;
      color: darkgray;
      text-align: center;
    }
    p{
      white-space: nowrap;
      color: black;
      text-align: center;
    }
  }
</style>
