<template>
  <div class="home-container">  
      <div class="first-content-container">
        <h1 class="header">HOW TO GO GREEN</h1>
        <br>
        <p class="paragrah-container"> 
        A lot of people are daunted by the idea of
          <strong>“going green”</strong> as it may seem like one would 
          need to make sweeping lifestyle changes to  
          be able to make a difference. Fortunately, 
          that’s not the case.
        </p>
        <div class="second-content-container">
          <h1 class="content-header">Want To Be Happier, Healthier, And More Productive? <br> Go Green.</h1>  
          <br>
          <p class="content">
            October is National Work & Family Month, when businesses, academic institutions, <br>
            federal agencies, members of Congress,work-life advocacy groups, and individuals collectively <br>
            raise awareness about making it easier for employees to succeed at work and at home. <br>
            We know a simple and extremely effective solution: Go green! As it turns out, going green <br>
            has plenty of benefits for more than just the planet.Research shows that green buildings <br>
            have a hugely positive impact on the health (mental and physical) of the lucky people who <br>
            live and work there.Going green means improving indoor <a href="https://elemental.green/?s=air+quality">air quality</a>, making use of natural lighting, <br>
            and using <a href="https://elemental.green/?s=eco-friendly+materials">eco-friendly materials</a> — all of which contribute to your happiness,health, and productivity. 
          </p>
        </div>
        <div class="third-content-container">
          <br><br><br><br>
          <h1 class="three-solutions">Three unbeatable solutions</h1>
          <p class="content-three-solutions">
              you back the most crucial solutions for our climate. Let’s revive ecosystems, <br> push green innovation, and support communities.
          </p>
          <v-card id="card-container">
            <ul class="bg-transparent">
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
                <img class="img-card" src="../assets/kidsinafrica4.jpg">
              </li>
            </ul>
          </v-card>
        </div>
        <div class="forth-content-container">
          <h1 class="company-topic"> 
            10 Top Companies That are "Going Green" <br> in 2020
          </h1>
          <br>
          <p class="company-content">
            Companies are therefore seeking more innovative methods of <br> 
            promoting eco-friendly environments by integrating green <br> 
            practices in their business functions. The following are the <br>
            top companies that are taking the lead in incorporating eco-friendly <br> 
            practices by going green.
          </p>
          <img class="img-company-logo" src="../assets/logo.jpg">
        </div>
        <hr>
        <div class="footer-container">
          <h1 class="footer-app-name">Ecofreak</h1>
          <div class="footer-navbar">
            <router-link class="link" to="/">Home</router-link> 
            <router-link class="link" to="/about">About</router-link> 
            <router-link class="link" to="/product">Product</router-link> 
            <router-link class="link" to="/blog">Blog</router-link>
          </div>
        </div>
      </div>
      <div class="image-container"> 
        <img class="img-header" alt="leaf-header" src="../assets/leaf2.jpg">
      </div>
  </div>  
</template>



<script>

</script>




<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Gothic+A1:wght@200;300;400&family=Josefin+Sans:ital,wght@0,200;1,500;1,700&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Gothic+A1:wght@200;300;400&family=Josefin+Sans:ital,wght@0,200;0,400;1,500&display=swap');
  
  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed, 
  figure, figcaption, footer, header, hgroup, 
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
  /* HTML5 display-role reset for older browsers */
  article, aside, details, figcaption, figure, 
  footer, header, hgroup, menu, nav, section {
    display: block;
  }
  body {
    line-height: 1;
  }
  ol, ul {
    list-style: none;
  }
  blockquote, q {
    quotes: none;
  }
  blockquote:before, blockquote:after,
  q:before, q:after {
    content: '';
    content: none;
  }
  table {
    border-collapse: collapse;
    border-spacing: 0;
  }
  strong {
    font-weight: bold;
  }

  .home-container{
    display: flex;
    flex-direction: row;
  }
  .first-content-container {
    width: 25%;
    margin-top: 10em; 
  }
  .header {
    width: 80%;
    text-align: left;
    margin-left: 6.5em;
    font-weight: 700;
    font-size: 150%;
    font-family: 'Josefin Sans', sans-serif;
  }
  .paragrah-container {
    text-align: left;
    margin-left: 10em;
    width: 80%;
    font-family: 'Josefin Sans', sans-serif;
  }
  .img-header {
    margin-left: 30em;
    margin-top: 5em;
    width: 55%;
  }
  .image-container {  
    height: 40%;
  }
  .second-content-container {
    width: 400%;
  }
  .content-header {
    margin-top: 15em;
    font-weight: 700;
    font-size: 150%;
    text-align: left;
    margin-left: 20em;
    font-family: 'Josefin Sans', sans-serif;
  }
  .content{
    text-align: left;
    margin-left: 30em;
    font-family: 'Josefin Sans', sans-serif;
  }
  .third-content-container{
    background-color: #f3f3f3;
    width: 400%;
    margin-top: 10em;
    list-style: none
  }
  ul {
    display: flex;
    justify-content:space-between;
    width: 1600px;
    height: 500px;
    margin-top: 10em; 
    margin-right: 0;  
  }
  .card {
    width: 150%;
    display: flex;
    flex-flow: row wrap;
    justify-items: center;
    list-style-type:none;
    grid-gap: 10px;
  }
  .list-card {
    align-items: center;
    width: 230px;
    height: 300px;
    margin: 0 auto;
    box-shadow: 0 5px 15px 6px rgb(156, 156, 156);
    border-radius: 25px;
    opacity: 0.9;
  }
  .img-card{
    width: 100%;
    height: 100%;
    border-radius: 25px;
  }
  .title-container {
    position: relative;
  }
  .title-text {
    position: absolute; 
    top: 30px; 
    left: 0; 
    width: 100%;
    font-size: 200%;
    font-weight: 700; 
    font-family: 'Josefin Sans', sans-serif;
    color: white;
  }
  .three-solutions{
    font-size: 300%;
    font-weight: 700;
    font-family: 'Josefin Sans', sans-serif;
  }
  .content-three-solutions {
    font-size: 150%;
    font-weight: 500;
    color: rgb(107, 107, 107);
    font-family: 'Josefin Sans', sans-serif;
  }
  .forth-content-container {
    width: 100%;
  }
  .company-topic {
    text-align: left;
    margin-top: 5em;
    font-weight: 700;
    font-size: 150%;
    font-family: 'Josefin Sans', sans-serif;
    margin-left: 26.5em;
    width: 200%;
  }
  .company-content {
    text-align: left;
    margin-left: 40em;
    width: 120%;
  }
  .img-company-logo {
    margin-top: 3em;
    width: 200%;
    margin-left: 30em;
  }
  hr {
    border-top: 1px solid lightgray;
    width: 1300px; 
    margin-left:35% !important; 
    margin-right:20% !important;
    margin-bottom: 2em;
  }

  .footer-container {
    margin-top: 12px;
    height: 52px;
    margin-left: 10em;
    width: 90em;
    display: flex;
    align-content: flex-end;
    justify-content: space-between;
  }

  .footer-app-name{
    font-weight: 700;
    font-size: 150%;
    font-family: 'Josefin Sans', sans-serif;
    margin-bottom: 2em;
  }

  .footer-navbar {
    margin: 0;
    width:  100em;
    display: flex;
    justify-content: space-evenly;
    margin-bottom: 2em;

    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;

  }

  a {
    color: #2c3e50;
  }
  a:hover, a:active, a:focus {
    color:#42b983;
  }


</style>




       
