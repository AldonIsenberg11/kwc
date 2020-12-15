<template>
  <div class="container">
    <section id="about">
      <h2>WHO WE ARE</h2>
      <hr>
      <v-carousel
      show-arrows="false"
            cycle>
    <v-carousel-item
      v-for="FacilityInfo of FacilityInfo"
      :key="FacilityInfo.Photos.formats.large"
      :src="'https://kwc-server-strapi.herokuapp.com' + FacilityInfo.Photos.formats.large.url"
    ></v-carousel-item>
  </v-carousel>
              <br>
      <br><br>
      <p>{{ FacilityInfo.Description }}</p>
      <br>
      <hr>
    </section>
    <div class="clr" />
  </div>
</template>

<script>
import infoQuery from '~/apollo/info'
export default {
  data () {
    return {
      FacilityInfo: [],
      query: ''
    }
  },
  apollo: {
    FacilityInfo: {
      prefetch: true,
      query: infoQuery
    }
  }
}
</script>
