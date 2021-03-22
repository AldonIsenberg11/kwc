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
          <img class="eventicon" :src="'/assets/kwclogo.png'">
          <h1>{{ event.name }}</h1>
          <div class="eventblurb">
            {{ event.date }}
            <br>
            <br>
            {{ event.description }}
            <br>
            <br>
          </div>
        </div>
          <div>
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
export default {
  data () {
    return {
      events: [
        { id: 1, name: 'Diamonds in the Rough', date: 'March 20-21, 2021', eventFlyer: 'http://eventURL.pdf', description: 'All girls divisions k-12.' + '\n' + 'Registration: $50 per wrestler until 3/18/21, $75 per wrestler after 3/18/21.  Contact Linda Weedon @ 719-322-2718 for more info.' },
        { id: 2, name: 'Folkstyle, Freestyle & Greco Training Club', date: 'Ongoing', eventFlyer: 'http://eventURL.pdf', description: 'Training in Freestyle, Greco and Folkstyle wrestling in Olathe, Kansas. Our club is designed to provide top tier training and coaching to athletes of all age groups. We are offering training opportunities throughout the duration of the spring and summer. Contact us for more info.' }
      ],
      query: ''
    }
  }
}
</script>
