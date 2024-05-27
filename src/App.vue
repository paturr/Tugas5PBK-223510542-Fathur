
<template>
  <div class="q-pa-md">
    <q-layout view="lHh lpr lFf"  class="shadow-2 rounded-borders">
      <q-header elevated>
        <q-toolbar class="glossy">
          <q-avatar>
            <img src="./assets/gtr.png">
          </q-avatar>
          <q-toolbar-title>toko gitar fathur</q-toolbar-title>
        </q-toolbar>
      </q-header>
      <q-page-container>
        <div class="q-pa-md">
          <q-carousel
      animated
      v-model="slide"
      navigation
      infinite
      :autoplay="autoplay"
      arrows
      transition-prev="slide-right"
      transition-next="slide-left"
      @mouseenter="autoplay = false"
      @mouseleave="autoplay = true"
    >
      <q-carousel-slide :name="1" img-src="./assets/promo1.jpg" />
      <q-carousel-slide :name="2" img-src="./assets/promo2.jpg" />
      <q-carousel-slide :name="3" img-src="./assets/promo3.jpg" />
      <q-carousel-slide :name="4" img-src="./assets/promo4.jpeg" />
    </q-carousel>
        </div>

    <q-card class="my-card">
      <img src="./assets/gitar1.jpg">

      <q-card-section>
        <div class="text-h6">Harga: 1.500.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-subtitle2">Gitar Akustik</div>
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <img src="./assets/gitar1.jpg">

      <q-card-section>
        <div class="text-h6">Harga: 1.950.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-subtitle2">Gitar Listrik</div>
      </q-card-section>
    </q-card>
    <q-card class="my-card">
      <img src="./assets/gitar4.jpg">

      <q-card-section>
        <div class="text-h6">Harga: 1.200.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-subtitle2">Gitar Clasic</div>
      </q-card-section>
    </q-card>

      </q-page-container>
      <q-footer elevated>
        <q-toolbar class="glossy" style="text-align: center;">
          <q-toolbar-title>Create by Fathur</q-toolbar-title>
        </q-toolbar>
      </q-footer>
    </q-layout>
  </div>
</template>
     
<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('style'),
      slide: ref(1),
      autoplay: ref(true)

    }
  }
}
</script>
<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
