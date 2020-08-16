<template>
  <div class="home-container">  
      <div class="first-container">
        <h1 class="header">HOW TO GO GREEN</h1>
        <p class="paragrah-container"> A lot of people are daunted by the idea of <strong>“going green”</strong> as it may seem like one would need to make sweeping lifestyle changes to be able to make a difference. Fortunately, that’s not the case.</p>
        <h3 class="content-header">Want To Be Happier, Healthier, And More Productive? Go Green.</h3>  
        <p class="content">October is National Work & Family Month, when businesses, academic institutions, federal agencies, members of Congress, work-life advocacy groups, and individuals collectively raise awareness about making it easier for employees to succeed at work and at home. We know a simple and extremely effective solution: Go green! As it turns out, going green has plenty of benefits for more than just the planet. Research shows that green buildings have a hugely positive impact on the health (mental and physical) of the lucky people who live and work there. Going green means improving indoor <a href="https://elemental.green/?s=air+quality">air quality</a>, making use of natural lighting, and using <a href="https://elemental.green/?s=eco-friendly+materials">eco-friendly materials</a> — all of which contribute to your happiness, health, and productivity. </p>
      <div class="card-container">
        <ul class="card">
          <li class="list-card">
            <div class="title-container">
              <h1 class="title-text">Nature</h1>
            </div>
            <img class="img-card" src="../assets/nature1.jpeg">
          </li>
          <li class="list-card">
            <div class="title-container">
              <h1 class="title-text">Technology</h1>
            </div>
            <img class="img-card" src="../assets/solarcell6.jpg">
          </li>
          <li class="list-card">
            <div class="title-container">
              <h1 class="title-text">Social</h1>
            </div>
            <img class="img-card" src="../assets/kidsinafica1.jpg">
          </li>
        </ul>
      </div>
      </div>
      <div class="image-container"> 
        <img class="img-header" alt="leaf-header" src="../assets/leaf2.jpg">
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
    width: 55%;
  }
  .image-container {  
    height: 40%;
  }
  .content-header {
    width: 50em;
    margin-top: 15em;
    margin-left: 13em;
  }
  .content{
    width: 50em;
    margin-left: 20em;
    text-align: left;
  }
  .card-container {
    display: flex;
 
    width: 1500px;
    height: 500px;
    margin-top: 10em; 
  }
  .card {
    width: 150%;
    display: flex;
    justify-content: space-between;
    list-style-type:none;
    grid-gap: 10px;
  }
  .list-card {
    align-items: center;
    width: 230px;
    height: 300px;
    margin: 0 auto;
    background-color: #f6faf6;
    box-shadow: 0 5px 15px 6px rgb(156, 156, 156);
    border-radius: 25px;
  }
  .img-card {
    width: 100%;
    height: 100%;
    border-radius: 25px;
  }
  .title-container {
    position: relative;
    color: white;
  }
  .title-text {
    position: absolute; 
    top: 40px; 
    left: 0; 
    width: 100%; 
  }


</style>



