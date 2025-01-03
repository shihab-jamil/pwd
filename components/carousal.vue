<script setup>

const carouselConfig = {
  itemsToShow: 2,
  wrapAround: true,
};
</script>

<template>
  <Carousel v-bind="carouselConfig">
    <Slide v-for="slide in 10" :key="slide">
      <div class="carousel__item">
        <div class="container">
          <img src="~/assets/carousal/image1.png" alt="Snow" style="width:100%;" class="image">
          <div class="overlay"></div>
          <div class="text">
            <div class="flex flex-col justify-between items-start h-full">
              <div class="flex flex-col items-start gap-1 py-4">
                <span class="text-3xl font-bold">Tribute 2.3</span>
                <span class="text-lg"><span class="opacity-50">Platform :</span> 2k24</span>
                <span class="text-lg"><span class="opacity-50">Category :</span> Tool</span>
              </div>
              <div>
                <div
                  class="flex flex-col px-4 py-4 text-gray-400 text-sm gap-3"
                >
                  <div class="flex items-center space-x-1">
                    <!-- Eye Icon -->
                    <Icon icon="hugeicons:view" class="text-white" width="24" height="24" />
                    <span class="text-white">123</span>
                  </div>

                  <div class="flex items-center space-x-1">
                    <!-- Eye Off Icon -->
                    <Icon icon="mingcute:download-3-line" class="text-white" width="24" height="24" />
                    <span class="text-white">321</span>
                  </div>
                  <h2 class="text-white"><span class="opacity-50">Submitted by</span> <strong>Robert kiddOX</strong></h2>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </Slide>

    <template #addons>
      <Navigation >
        <template #prev>
          <Icon
            icon="mynaui:arrow-left-square-solid"
            width="64"
            height="64"
            color="white"
          />
        </template>
        <template #next>
          <Icon
            icon="mynaui:arrow-right-square-solid"
            width="64"
            height="64"
            color="white"
          />
        </template>
      </Navigation>
      <Pagination />
    </template>
  </Carousel>
</template>

<style>
:root {
  --carousel-transition: 300ms;
  --carousel-opacity-inactive: 0.7;
  --carousel-opacity-active: 1;
  --carousel-opacity-near: 0.9;
  --vc-pgn-active-color : white;
}

.carousel__viewport {
  perspective: 2000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: opacity var(--carousel-transition),
  transform var(--carousel-transition);
}

.carousel.is-dragging .carousel__slide {
  transition: opacity var(--carousel-transition),
  transform var(--carousel-transition);
}

.carousel__slide {
  opacity: var(--carousel-opacity-inactive);
  transform: translateX(10px) rotateY(-12deg) scale(0.9);
}

.carousel__slide--prev {
  opacity: var(--carousel-opacity-near);
  transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--active {
  opacity: var(--carousel-opacity-active);
  transform: rotateY(0) scale(1);
}

.carousel__slide--next {
  opacity: var(--carousel-opacity-near);
  transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--next ~ .carousel__slide {
  opacity: var(--carousel-opacity-inactive);
  transform: translateX(-10px) rotateY(12deg) scale(0.9);
}

.carousel__prev, .carousel__next{
  height: unset !important;
  width: unset !important;
}

.container {
  position: relative;
  overflow: hidden;
}
.image {
  width: 100%;
  height: auto;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 70%; /* Half of the image */
  height: 100%;
  background: linear-gradient(to right, rgba(0, 0, 0, .9), rgba(0, 0, 0, 0)); /* Fading effect */
  border-radius: 10px 0 0 10px;
}
.text {
  position: absolute;
  top: 0;
  left: 10px;
  color: white;
  font-size: 24px;
  font-weight: bold;
  height: 100%;
}
</style>
