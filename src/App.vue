<template>
  <v-app>
    <!-- Header component -->
    <HeaderComponent></HeaderComponent>
    <!-- Header component end -->
    <!-- banner-section -->
    <v-row class="d-flex flex-column grey-bg banner mt-16 pb-7 container-width">
      <v-col class="cols-12 text-center d-flex flex-column align-center">
        <h4 class="text-uppercase font-weight-light mb-4 sub-title">Shopify experts</h4>
        <h1 class="mb-6">Et dedikeret e-commerce-bureau</h1>
        <v-img class="banner-image" :src="require('@/assets/images/banner-image.png')"></v-img>
      </v-col>
    </v-row>
    <!-- banner section end -->
    <!-- grid section -->
    <v-row class="my-lg-16 justify-center">
      <v-col class="text-center" cols="12" lg="8">
        <h2 class="mb-2">Kompetencer</h2>
        <p>Ved at kombinere analyse, strategi, kreativitet, design og udvikling, skaber vi positiv gennemslagskraft for
          ambitiøse brands, som ønsker at opnå målbar afkast.</p>
      </v-col>
    </v-row>
    <div :class="!$vuetify.display.mobile ? 'row-reverse justify-space-between container-width mb-10' : 'justify-center'">
      <div>
        <v-img width="600" :src="require('@/assets/images/webdesign.png')"></v-img>
      </div>
      <div :style="$vuetify.display.mobile ? 'width:100%' : 'max-width:553px'"
        :class="$vuetify.display.mobile ? 'text-center' : 'd-flex flex-column align-start justify-center'">
        <h3 class="my-3">Webdesign</h3>
        <p class="mb-4">Vi skaber mindeværdige brugeroplevelser og øget salg med unikt webdesign.
        </p>
        <v-btn class="primary-btn mb-3">Læs mere</v-btn>
      </div>
    </div>
    <div
      :class="!$vuetify.display.mobile ? 'd-flex flex-row justify-space-between container-width mb-16' : 'justify-center'">
      <div class="d-flex justify-start">
        <v-img class="grid-img" width="600" :src="require('@/assets/images/webudvikling.png')"></v-img>
      </div>
      <div :style="$vuetify.display.mobile ? 'width:100%' : 'max-width: 553px'"
        :class="$vuetify.display.mobile ? 'text-center' : 'd-flex flex-column align-end justify-center'">
        <h3 class="my-3">Webudvikling i Shopify</h3>
        <p class="mb-4 text-end">Vi er certificerede Shopify eksperter og udvikler mindeværdige e-commerce løsninger
        </p>
        <v-btn class="primary-btn mb-3">Læs mere</v-btn>
      </div>
    </div>
    <!-- grid section end -->
    <!-- image section -->
    <v-row class="mt-lg-16">
      <v-col class="text-center">
        <h2 class="mb-lg-16 mb-5">Arbejdskulturen hos Grafikr</h2>
        <v-col :class="$vuetify.display.mobile ? null : 'work-culture-image'" class="grey-bg">
          <v-img :src="require('@/assets/images/work-culture.png')"></v-img>
        </v-col>
      </v-col>
    </v-row>
    <!-- image section end -->
    <!-- carousel section  -->
    <v-row>
      <v-col class="text-center">
        <h2 class="mb-10 mt-lg-16">Arbejd med nogle af de største brands</h2>
      </v-col>
    </v-row>
    <CarouselComponent></CarouselComponent>
    <!-- carousel section end  -->

    <!-- colleagues section  -->
    <v-row class="d-flex flex-column my-16">
      <v-col class="text-center">
        <h2>Mød dine (Måske) nye kollegaer</h2>
      </v-col>
      <v-col class="d-flex justify-center text-center">
<div style="width: 700px;">
<div class="container">
  <span class="name mr-2">Kiranan,</span>
  <img class="overlay-image" :src="require('@/assets/images/kiranan.png')">
  
</div>
<div class="container">
  <span class="name  mr-2">Erik,</span>
  <img class="overlay-image" :src="require('@/assets/images/erik.png')">
  
</div>
  <span class="name mr-2 mb-5">Lasse,</span>
  <span class="name mr-2">Pernille,</span>
  <span class="name mr-2">Magnus,</span>
  <span class="name mr-2">Rasmus,</span>
  <span class="name mr-2">Christian,</span>
  <span class="name mr-2">Tobias,</span>
  <span class="name mr-2">Tor,</span>
  <span class="name mr-2">Thomas</span>
</div>
      </v-col>
    </v-row>
    <!-- colleagues section end  -->

    <!-- footer component  -->
    <FooterComponent></FooterComponent>
    <!-- footer component end  -->


  </v-app>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import FooterComponent from "./components/FooterComponent.vue"
import CarouselComponent from "./components/CarouselComponent.vue"
export default {
  name: "App",

  components: {
    HeaderComponent,
    FooterComponent,
    CarouselComponent
  },


};
</script>

<style >
@import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;1,200;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

.sub-title {
font-size: 14px;
}

.container {
  position: relative;
  display: inline-block;
}

.name {
  display: inline-block;
}

.overlay-image {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: opacity 0.5s ease;
  z-index: 9999;
  width: 200px;
  height: 200px;
}

.container:hover .overlay-image {
  opacity: 1;
}

.container-width {
  padding: 0 4em;
}

body {
  font-family: 'Plus Jakarta Sans', sans-serif;
}

h1 {
  font-size: 48px;
}

h2 {
  font-size: 36px;
}

h3 {
  font-size: 32px;
  font-weight: 400;
}

h4 {
  font-size: 16px;
}

p {
  font-size: 24px;

}

.work-culture-image {
  padding: 5em;
}


.banner {
  padding-top: 10em;
}

.banner-image {
  width: 100%
}

.grey-bg {
  background-color: #F6F4F4;
}

.carousel-title {
  color: #ffff;
  font-size: 24px;
  position: absolute;
}

.row-reverse {
  display: flex;
  flex-direction: row-reverse;
}

.colleagues-list {
  margin-bottom: 7em;
  width: 1000px;
}


.name {
  display: inline-block;
  font-size: 36px;
}


@media only screen and (max-width: 600px) {
  h1 {
    font-size: 24px;
  }

  h2 {
    font-size: 20px;
  }

  h3 {
    font-size: 18px;
  }

  h4 {
    font-size: 16px;
  }

  p {
    font-size: 14px;
    padding: 0 30px;
  }

  .v-row {
    padding: 10px;
  }

  .colleagues-list li {
    display: inline-block;
    font-size: 16px;
  }

}
</style>
