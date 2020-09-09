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
      the Earth and her resources—the way we relate to the Earth as separate, non-living, and unlimited. I believe that we can <br> 
      transform our relationship to the Earth. Instead of seeing the Earth as outside ourselves, we can see the Earth as our <br>  
      extended body, our home. Perhaps then, we would take care of her the way we would take care of our own body.
      </p>
      <br>
      <hr>
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
    height: 1500px;
  }
  .about-content {
    margin-left: 30em;
    text-align: left;
  }
  hr {
    width: 70%;
  }
</style>

