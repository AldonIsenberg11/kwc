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
          <div class="newscard">
            <div class="newsicon">
              <iframe
                src="https://www.facebook.com/plugins/video.php?height=476&href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter%2Fvideos%2F1026246774509319%2F&show_text=false"
                height="400px"
                allow="encrypted-media"
                allowFullScreen="true"
              />
              <br>
            </div>
            <div class="eventblurb">
              Mats are here!!!
              <br>
              <br>
              Starting to come together
            </div>
          </div>
          <div class="newscard">
            <div class="newsicon">
              <iframe
                height="400px"
                src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter%2Fposts%2F124466549440738&show_text=false"
                allow="encrypted-media"
                allowFullScreen="true"
              />
              <br>
            </div>
            <div class="eventblurb">
              Practice has Started
              <br>
              <br>
              KWC welcomes the Trailblazer Kids Club out of Gardner as our 1st practice group
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
          <img class="eventicon" :src="'https://kwc-server-strapi.herokuapp.com' + event.Picture.formats.thumbnail.url">
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

<style>

</style>
