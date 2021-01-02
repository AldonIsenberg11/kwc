<template>
  <div class="container">
    <section id="about">
      <h2>WHO WE ARE</h2>
      <hr>
      <v-carousel show-arrows-on-hovercycle>
      <v-carousel-item
        v-for="facilityInfo of facilityInfo"
        :key="facilityInfo.Photos"
        :src="'https://kwc-server-strapi.herokuapp.com' + facilityInfo.Photos"
      ></v-carousel-item>
  </v-carousel>
      <br>
      <br><br>
      <p>{{ facilityInfo.Description }}</p>
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
      facilityInfo: [],
      query: ''
    }
  },
  apollo: {
    facilityInfo: {
      prefetch: true,
      query: infoQuery
    }
  }
}
</script>
