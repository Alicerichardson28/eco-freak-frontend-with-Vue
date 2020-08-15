<template>
  <div class="home-container">  
      <div class="first-container">
        <h1 class="header">HOW TO GO GREEN</h1>
        <p class="paragrah-container"> A lot of people are daunted by the idea of <strong>“going green”</strong> as it may seem like one would need to make sweeping lifestyle changes to be able to make a difference. Fortunately, that’s not the case.</p>
        <p class='content'>Want To Be Happier, Healthier, And More Productive? Go Green.</p>  
      </div>
      <div class="image-container"> 
        <img class="img-header" alt="leaf-header" src="../assets/leaf2.jpg">
      </div>
      <div>
      </div>
  </div>  
</template>

<script>
  // import SecondHome from '../views/SecondHome'
  // export default {
  //   name: 'home',
  //   components: {
  //       SecondHome
  //   }
  // }
</script>

<style scoped>
  .home-container {
    display: flex;
    flex-direction: row;
    margin-left: 10em;
  }
  .first-container {
    width: 25%;
    margin-top: 10em;
  }
  .header {
    text-align: left;
  }
  .paragrah-container {
    text-align: left;
  }
  .img-header {
    margin-left: 30em;
    margin-top: 5em;
    width: 60%;
  }
  .image-container {  
    height: 40%;
  }
  .content {
    width: 70%;
    margin-top: 30em;
    margin-left: 30em;
  }
</style>



