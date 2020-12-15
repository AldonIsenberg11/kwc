<template>
  <div class="container">
     <section id="eventpage">
      <h2>LATEST NEWS</h2>
      <hr>
      <br>
      <div class="newsgrid">
      <div class="newsbox">
        <div v-for="categories of categories" :key="categories.id" class="newscard1">
          <img class="eventicon" :src="'https://kwc-server-strapi.herokuapp.com' + categories.media.formats.thumbnail.url">
           <div class="eventblurb">
            <h1>{{ categories.Name }}</h1>
            {{ categories.Date }}
            <br>
            <br>
            {{ categories.Description }}
          </div>
          <!-- comment out until needed to create event page -->
          <!-- <div class="moreInfoButton" @click="$router.push(`/events/${event.id}`)">
            MORE INFO
          </div> -->
        </div>
      </div>
      <div id=facebookfeed>
      <iframe
      src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2Fkswrestlingcenter&tabs=timeline&width=300&height=900&small_header=true&adapt_container_width=true&hide_cover=true&show_facepile=true&appId"
      width="300"
      height="900"
      style="border:none;overflow:hidden"
      scrolling="no"
      frameborder="0"
      allowfullscreen="true"
      allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share">
      </iframe>
      </div>
      </div>
      </section>
    <div class="clr" />
    <hr>
  </div>
</template>
<script>
import newsQuery from '~/apollo/news'
export default {
  data () {
    return {
      categories: [],
      query: ''
    }
  },
  apollo: {
    categories: {
      prefetch: true,
      query: newsQuery
    }
  }
}
</script>
