<template>
  <div class="container">
    <section id="eventpage">
      <h2>UPCOMING EVENTS</h2>
      <hr>
      <br>
      <div v-if="events.length === 0">
        Currently no events to display
      </div>
      <div v-else class="eventbox">
        <div v-for="event of events" :key="event.id" class="eventcard">
          <img class="eventicon" :src="'https://kwc-server-strapi.herokuapp.com' + event.Picture.formats.thumbnail.url">
          <h1>{{ event.Title }}</h1>
          <div class="eventblurb">
            {{ event.Date }}
            <br>
            <br>
            {{ event.Description }}
          </div>
          <!-- comment out until needed to create event page -->
          <!-- <div class="moreInfoButton" @click="$router.push(`/events/${event.id}`)">
            MORE INFO
          </div> -->
        </div>
      </div>
      <br>
      <br>
      <br>
      <hr>
    </section>
    <div class="clr" />
  </div>
</template>

<script>
// import eventsQuery from '~/apollo/events'
export default {
  data () {
    return {
      events: [],
      query: ''
    }
  }
  // apollo: {
  //   events: {
  //     prefetch: true,
  //     query: eventsQuery
  //   }
  // }
}
</script>
