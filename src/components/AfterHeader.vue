<template>
 
<div>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="480"
  >
    <b-carousel-slide
      caption="The secret of getting ahead is getting started"
      img-src="https://picsum.photos/1024/240/?random=1"></b-carousel-slide>
    <b-carousel-slide
      caption="There is nothing so fatal to character as half finished tasks"
      img-src="https://picsum.photos/1024/240/?random=12"></b-carousel-slide>
    <b-carousel-slide
      caption="The greater the effort, the greater the glory"
      img-src="https://picsum.photos/1024/240/?random=13"></b-carousel-slide>
  </b-carousel>
</div>
</template>

<style lang="scss">

.size {
    font-size: 250%;  
   }
</style>