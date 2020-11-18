<template>
<div class="container">
<section id="eventpage">
                  <h2>UPCOMING EVENTS</h2>
                  <hr>
                  <br>
                  <p>Coming soon!</p>
                  <br>
                  <div class="eventbox">
                  <div
                    class="eventcard"
                    v-for="event of events"
                    :key="event.id"
                    >
                    <img
                    class="eventicon"
                      :src="'http://localhost:1337' + event.Picture.formats.thumbnail.url"
                    />
                    <h1>{{ event.Title}}</h1>
                    <div class="eventblurb">{{ event.Date }}<br><br>{{ event.Description }}</div>
                    <div
                    class="button"
                        @click="$router.push(`/events/${event.id}`)"
                        >
                        MORE INFO
                    </div>
                  </div>
                   </div>
                  <br><br><br>
                  <hr>
              </section>
              <div class="clr"></div>
              </div>
              </template>

<script>
import eventsQuery from '~/apollo/events'
export default {
  data () {
    return {
      events: [],
      query: ''
    }
  },
  apollo: {
    events: {
      prefetch: true,
      query: eventsQuery
    }
  }
}
</script>
