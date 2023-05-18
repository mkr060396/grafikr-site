<template>
  <div>
    <v-app-bar dark flat :class="$vuetify.display.mobile ? 'px-0 ' : 'fixed'" color="#F6F4F4">
      <v-app-bar-nav-icon v-if="$vuetify.display.mobile" @click="drawer = true"></v-app-bar-nav-icon>
      <div>
        <img :src="require('@/assets/images/Logo.png')">
      </div>

      <div v-if="!$vuetify.display.mobile">
        <v-btn text class="nav-link">Forside</v-btn>
        <v-btn text class="nav-link">Kompetencer</v-btn>
        <v-btn text class="nav-link">Cases</v-btn>
        <v-btn text class="nav-link">Blog</v-btn>
        <v-btn text class="nav-link">Om os</v-btn>
        <v-btn text class="nav-link">Kontakt</v-btn>
      </div>

      <div v-if="!$vuetify.display.mobile">
        <v-btn dark class="primary-btn">Hent e-bog
        </v-btn>
      </div>
    </v-app-bar>

    <v-navigation-drawer class="mobile-nav" v-model="drawer" absolute color="#F6F4F4" temporary>
      <v-list nav dense>
        <v-list-item-group v-model="group">
          <v-list-item>
            <v-list-item-title><a href="#">Forside</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><a href="#">Kompetencer</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><a href="#">Cases</a> </v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title> <a href="#">Blog</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><a href="#">Om os</a></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><a href="#">Kontakt</a></v-list-item-title>
          </v-list-item>
          
          <v-list-item>
            <v-list-item-title>    <v-btn dark class="primary-btn">Hent e-bog
        </v-btn></v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script  setup>
import { ref } from "vue";
const drawer = ref(false)
const group = null

</script>

<style>
.v-toolbar__content {
display: flex; 
justify-content: space-between;
padding: 0 4em;
}
.nav-link {
  text-transform: initial;
  font-size: 14px;
  border-radius: 0px;
}
.nav-link:hover {
  border-bottom: 2px solid black;
}
.primary-btn {
  background-color: black;
  color: white !important;
  text-transform: inherit;
  border-radius: 2px;
  font-size:14px;
}

.mobile-nav a {
  color: black
}

@media only screen and (max-width: 600px) {
  .v-toolbar__content {
display: flex; 
justify-content: start;
padding: 0;
}

}
</style>