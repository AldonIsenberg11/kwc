<template>
  <div>
    <section id="banner">
      <div id="biglogo">
        <div />
        <bwords>Winning is the goal. <br><br>Wrestling is the journey.<br><br>Are you ready?</bwords>
        <img src="../assets/largelogo.png">
        <div />
      </div>
    </section>
    <div class="clr" />
    <section id="welcome">
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
          <!-- <div class="newscard"><div class="newsicon"><img height=100px src="../assets/boxingring.png" alt="Event"><br></div>MMA Maybe<br><br>Nov 6th. Get you tickets now. Selling out fast!</div> -->
        </div>
        <NuxtLink to="/news" class="button">
          READ MORE
        </NuxtLink>
      </div>
    </section>
    <section id="upcomingevents">
      <div class="content">
        <h3>Upcoming Events</h3>
        <br>
        <div class="eventpreview">
          <div v-for="event of events" :key="event.id" class="eventcard">
            {{formattedUrl(event.Picture.formats.thumbnail.url)}}
          <img class="eventicon" :src="formattedUrl(event.Picture.formats.thumbnail.url)">
          <h1>{{ event.Title }}</h1>
          <div class="eventblurb">
            {{ event.Date }}
            <br>
          </div>
          <NuxtLink to="/events" class="moreInfoButton" @click="$router.push(`/events/${event.id}`)">
            MORE INFO
          </NuxtLink>
        </div>
        </div>
        <NuxtLink to="/events" class="button2">
          GO TO EVENTS PAGE
        </NuxtLink>
      </div>
    </section>
    <!-- <section id="affiliates">
      <div class="content">
        <h2>Affiliates</h2>
        <br>
        <div class="linkbanner">
          <div><img src="../assets/logo1.png" alt="Event"></div>
          <div><img src="../assets/logo2.png" alt="Event"></div>
          <div><img src="../assets/logo3.png" alt="Event"></div>
          <div><img src="../assets/logo4.png" alt="Event"></div>
          <div><img src="../assets/logo5.png" alt="Event"></div>
        </div>
      </div>
    </section> -->
    <section id="quickcontact">
      <div class="content">
        <h3>Stay in the know</h3>
        <br>
        <br>
        <form id="form2">
          <div>
            <label>First Name</label>
            <input type="text" name="firstName" placeholder="Enter first name">
          </div>
          <div>
            <label>Last Name</label>
            <input type="text" name="lastName" placeholder="Enter last name">
          </div>
          <div>
            <label>Email</label>
            <input type="email" name="email" placeholder="champ@wrestleDB.com">
          </div>
          <div class="button">
            <br>
            <button type="submit" name="submit">
              --->Join our mailing list!
            </button>
          </div>
        </form>
        <br>
        <br>
      </div>
      <br>
      <div class="clr" />
    </section>
  </div>
</template>

<script>
import eventsQuery from '~/apollo/events'
import newsQuery from '~/apollo/news'
export default {
  methods: {
    formattedUrl: (url) => {
      let baseUrl = 'http://localhost:1337'

      if (process.env.KWC_SERVER_URL) {
        baseUrl = process.env.KWC_SERVER_URL
      }

      return baseUrl + url
    }
  },
  data () {
    return {
      events: [],
      query: '',
      categories: []
    }
  },
  apollo: {
    events: {
      prefetch: true,
      query: eventsQuery
    },
    categories: {
      prefetch: true,
      query: newsQuery
    }
  }
}
</script>

<style>

</style>
