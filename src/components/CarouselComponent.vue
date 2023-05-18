<template>
  <vueper-slides :arrows-outside="false" class="no-shadow" :visible-slides="3" slide-multiple :gap="4"
    :breakpoints="{ 600: { visibleSlides: 1, slideRatio: 1, } }">
    <vueper-slide v-for="item in items" :key="item.id" :image="item.image" :title="item.title" />
  </vueper-slides>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
export default {

  components: {
    VueperSlides,
    VueperSlide
  },

  data: () => ({
    items: [
      {
        id: 1,
        image: require('@/assets/images/barons.png'),
        title: 'Barons'
      },
      {
        id: 2,
        image: require('@/assets/images/basic-apparel.png'),
        title: 'Basic Apparel'
      },
      {
        id: 3,
        image: require('@/assets/images/shaping-new-tomorrow.png'),
        title: 'Shaping New Tomorrow'
      },
      {
        id: 4,
        image: require('@/assets/images/barons.png'),
        title: 'Barons'
      },
      {
        id: 5,
        image: require('@/assets/images/basic-apparel.png'),
        title: 'Basic Apparel'
      },
      {
        id: 6,
        image: require('@/assets/images/shaping-new-tomorrow.png'),
        title: 'Shaping New Tomorrow'
      },

    ]
  }),
}
</script>

<style>
.vueperslides__arrow svg {
  border: 2px solid white;
  border-radius: 50%;
  width: 120px;
  height: 120px;
}

.vueperslide__content-wrapper {
  display: flex !important;
  justify-content: end !important;
  align-items: flex-start !important;
  padding: 10px;
  color: white;
  font-size: 24px;
}

@media only screen and (max-width: 600px) {

  .vueperslides__arrow svg {
    display: none;
  }

  .vueperslide__content-wrapper {
    display: flex !important;
    justify-content: end !important;
    align-items: flex-start !important;
    color: white;
    font-size: 12px;
  }
}
</style>