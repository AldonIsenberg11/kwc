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
          <img class="eventicon" :src="event.logoUrl">
          <h1>{{ event.name }}</h1>
          <div class="eventblurb">
            {{ event.date }}
            <br>
            <br>
            {{ event.description }}
            <br>
            <br>
          <a v-if="event.signup" :href="event.signup" target="__blank">
                  SIGN UP
                </a>
                <br>
          <a v-if="event.eventFlyer" :href="event.eventFlyer" target="__blank">
                  VIEW FLYER
                </a>
                <br>
        </div>
        </div>
        <br>
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
import wrestlingEvents from '~/services/eventService.js'
export default {
  head () {
    return {
      title: 'Events'
    }
  },
  data () {
    return {
      events: wrestlingEvents,
      query: ''
    }
  }
}
</script>
