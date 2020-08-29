<template>
<mdb-carousel
    :items="thumbnailCarousel"
    thumbnails
    :interval="3000"
  ></mdb-carousel>
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
              "https://mdbootstrap.com/img/Photos/Slides/img%20(88).jpg",
            thumbnail:
              "https://mdbootstrap.com/img/Photos/Others/Carousel-thumbs/img%20(88).jpg"
          },
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
              "https://mdbootstrap.com/img/Photos/Slides/img%20(121).jpg",
            thumbnail:
              "https://mdbootstrap.com/img/Photos/Slides/img%20(121).jpg"
          },
        ]
      };
    }
  };
</script>

