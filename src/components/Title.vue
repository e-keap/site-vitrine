<template>
  <h1 class="ekeap-title">{{ titre }}</h1>
</template>

<script>
  export default {
    props: {
      titre: {
        type: String,
        default: () => 'I am Groot'
      },
    }
  }
</script>

<style lang="scss" scoped>
  .ekeap-title{
    font-size: 52px;
    color: #3837D3;
    font-weight: 700;
    // background: rgba(241,120,81,1);
    text-transform: uppercase;
    padding-left: 50px;
    position: relative;
    margin: 50px 0 100px 0;

    &::before{
      content: '';
      position: absolute;
      background: #F17851;
      left: -170px;
      border-radius: 500px;
      top: 0;
      width: 200px;
      height: 100%;
    }
    &::after{
      content: '';
      position: absolute;
      background: darkgrey;
      left: 200px;
      border-radius: 500px;
      bottom: -10px;
      width: 3000px;
      height: 5px;
    }
  }
</style>