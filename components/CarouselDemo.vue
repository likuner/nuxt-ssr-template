<template>
  <h3>Carousel</h3>
  <Carousel autoplay v-model="value" loop>
    <CarouselItem>
      <div class="demo-carousel">1</div>
    </CarouselItem>
    <CarouselItem>
      <div class="demo-carousel">2</div>
    </CarouselItem>
    <CarouselItem>
      <div class="demo-carousel">3</div>
    </CarouselItem>
    <CarouselItem>
      <div class="demo-carousel">4</div>
    </CarouselItem>
  </Carousel>
</template>
<script>
export default {
  data () {
    return {
      value: 0
    }
  }
}
</script>
