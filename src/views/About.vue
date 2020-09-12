<template>
  <div class='about-container'> 
    <mdb-carousel class='about'
        :items="thumbnailCarousel"
        thumbnails
        :interval="3000"
      ></mdb-carousel>
      <br>
      <h1>Gentle on Our Bodies and Our Earth</h1>
      <br>
      <p class='about-content'>
      We are living in a time of turmoil for the Earth. Species extinction, deforestation, climate change, rising sea levels, <br> 
      and many other problems face the planet we call home. These problems are a result of the way modern society exploits <br> 
      the Earth and its resources—the way we relate to the Earth as separate, non-living, and unlimited. I believe that we can <br> 
      transform our relationship to the Earth. Instead of seeing the Earth as outside ourselves, we can see the Earth as our <br>  
      extended body, our home. Perhaps then, we should take care of it the way we would take care of our own body.
      </p>
      <br>
      <hr>
      <br>
      <h2>50 Ways to Help the Planet - <br> Save Our Environment and Planet Earth</h2>
      <br>
      <p>According to <a href="https://www.50waystohelp.com/"> 50 ways to help.com </a> you can help to save this world. <br> 
      When you hear the words "saving the planet" it soundes big doesn't it? <br> 
      But this website will show you how to save the world in simple easy to understand ways. <br> 
      We can accomplish great feats, with small changes if we do them collectivly.  
      </p>
      <br><br><br>
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
</template>

<script>
  import { mdbCarousel } from "mdbvue";
  export default {
    name: "ThumbnailsCarouselPage",
    components: {
      mdbCarousel
    },
    data() {
      return {
        thumbnailCarousel: [
            {
            img: true,
            src:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(45).jpg",
            thumbnail:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(45).jpg"
          },
          {
            img: true,
            src:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(88).jpg",
            thumbnail:
              "https://mdbootstrap.com/img/Photos/Others/Carousel-thumbs/img%20(88).jpg"
          },
          {
            img: true,
            src:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(16).jpg",
            thumbnail:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(16).jpg"
          },
        ]
      };
    }
  };
</script>

<style lang="scss" scoped>
  .about-container {
    height: 1400px;
  }
  .about-content {
    margin-left: 30em;
    text-align: left;
  }
  hr {
    width: 70%;
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

