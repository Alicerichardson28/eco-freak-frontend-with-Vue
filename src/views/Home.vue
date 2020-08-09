<template>
  <div class="home-container">
    <div class="header-container">
      <h1>HOW TO GO GREEN</h1>
      <p class="paragrah-container"> A lot of people are daunted by the idea of “going green” as it may seem like one would need to make sweeping lifestyle changes to be able to make a difference. Fortunately, that’s not the case.</p>
    </div>
    <div class="image-container"> 
      <img class="img-header" alt="leaf logo" src="../assets/leaf2.jpg">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

// export default {
//   name: 'Home',
//   components: {
    
//   }
// }
</script>

<style scoped>
  .home-container {
    display: flex;
    flex-direction: row;
    margin-left: 10em;
  }
  .header-container {
    width: 25%;
    margin-top: 10em;
  }
  .img-header {
    margin-left: 30em;
    margin-top: 5em;
    width: 57%;
  }
</style>