<template>
  <div>
    <section id="banner">
      <div id="biglogo">
        <div v-show="$vuetify.breakpoint.mdAndUp" />
        <span>Winning is the goal. <br><br>Wrestling is the journey.<br><br>Are you ready?</span>
        <img v-show="$vuetify.breakpoint.mdAndUp" src="../assets/largelogo.png">
        <div v-show="$vuetify.breakpoint.mdAndUp" />
      </div>
    </section>
    <!-- <div class="clr" /> -->
    <section>
      <v-row>
        <v-col v-show="$vuetify.breakpoint.mdAndUp" md="2" />
        <v-col md="8">
          <iframe
            class="google-map"
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12421.17655703115!2d-94.7903587!3d38.8943885!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x892dbb21abb0db5a!2sKansas%20Wrestling%20Center!5e0!3m2!1sen!2sus!4v1609179719983!5m2!1sen!2sus"
            width="600"
            height="450"
            frameborder="0"
            style="border:0;"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
          />
        </v-col>
        <v-col v-show="$vuetify.breakpoint.mdAndUp" md="2" />
      </v-row>
    </section>
    <section align="center">
      <v-btn class="google-map" to="news">
        Read Latest News
      </v-btn>
    </section>
    <!-- <section id="welcome">
      <div class="content">
        <h2>Latest News</h2>
        <br>
        <div class="newspreview">
          <div v-for="categories of categories" :key="categories.id" class="newscard">
          <img class="eventicon" :src="formattedUrl(categories.media.formats.thumbnail.url)">
           <div class="eventblurb">
            <h1>{{ categories.Name }}</h1>
            {{ categories.Date }}
            <br>
            <br>
            {{ categories.Description }}
          </div>
          </div>
          <div class="newscard"><div class="newsicon"><img height=100px src="../assets/boxingring.png" alt="Event"><br></div>MMA Maybe<br><br>Nov 6th. Get you tickets now. Selling out fast!</div>
        </div>
        <v-btn :to="'/news'">READ MORE</v-btn>
      </div>
    </section> -->
    <section id="upcomingevents">
      <div class="content">
        <h3>Upcoming Events</h3>
        <br>
        <div class="eventpreview">
          <div v-for="event of events" :key="event.id" class="eventcard">
            <img class="eventicon" :src="event.imageUrl">
            <h1>{{ event.title }}</h1>
            <div class="eventblurb">
              {{ event.date }}
              <br>
            </div>
            <NuxtLink to="/events" class="moreInfoButton" @click="$router.push(`/events/${event.id}`)">
              MORE INFO
            </NuxtLink>
          </div>
        </div>
        <v-btn to="events">
          Go To Events Page
        </v-btn>
      </div>
    </section>
    <section id="quickcontact">
      <div class="content">
        <h3>Stay in the know</h3>
        <br>
        <br>
        <v-form>
          <input v-model="visitorName" class="stayInKnow" type="text" name="name" placeholder="Enter name">
          <input v-model="visitorEmail" class="stayInKnow" type="email" name="email" placeholder="champ@yourEmail.com">
          <br>
          <v-btn name="submit" @click="submitInformation()">
            Join our mailing list!
          </v-btn>
        </v-form>

        <br>
        <br>
      </div>
      <br>
      <div class="clr" />
    </section>
  </div>
</template>

<script>
// import eventsQuery from '~/apollo/events'
// import newsQuery from '~/apollo/news'
export default {
  data () {
    return {
      visitorName: '',
      visitorEmail: '',
      events: [
      ],
      query: '',
      categories: []
    }
  },
  methods: {
    // formattedUrl: (url) => {
    //   let baseUrl = 'http://localhost:1337'

    //   if (process.env.KWC_SERVER_URL) {
    //     baseUrl = process.env.KWC_SERVER_URL
    //   }

    //   return baseUrl + url
    // },
    // async submitInformation () {
    submitInformation () {
      const visitor = { name: this.visitorName, email: this.visitorEmail }
      // eslint-disable-next-line
      console.log('visitor:', visitor)
      // const result = await this.$axios.$post('/mailingList', visitor)
      // console.log('Need to add this to the database:', result)
      // console.log('This await:', result)
    }
  }
  // apollo: {
  //   events: {
  //     prefetch: true,
  //     query: eventsQuery
  //   },
  //   categories: {
  //     prefetch: true,
  //     query: newsQuery
  //   }
  // }
}
</script>

<style>
.stayInKnow {
  color: white;
}
</style>
