<template>
  <div>
      <body>
        <div id="app">
          <v-app>
            <v-main>
              <section id="hero">
                  <v-img
                  height="475"
                  src="https://scontent-dfw5-2.xx.fbcdn.net/v/t1.0-9/121015140_103253078228752_7405710129881532891_o.jpg?_nc_cat=104&_nc_sid=e3f864&_nc_ohc=V7hIRNO8R10AX8fR-0W&_nc_ht=scontent-dfw5-2.xx&oh=c6ac62f532eb2e8213b304400c31459e&oe=5FAB8252"
                  >
                                        <v-overlay absolute><bannertitle class="bannertag">LET'S WRESTLE</bannertitle></v-overlay></v-img>
              </section>

              <section>
                <div class="py-12"></div>

                <v-container class="text-center">
                  <h2 class="display-2 font-weight-bold mb-3">
                    LATEST NEWS
                  </h2>

                  <v-responsive class="mx-auto mb-12" width="56" align-center>
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive><br>
                </v-container>
                <v-container><v-col>
                  <iframe
                  src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter%2Fvideos%2F2840448136236421%2F&show_text=false&width=734&height=551&appId"
                  width="534"
                  height="351"
                  style="border:none;overflow:hidden"
                  scrolling="no"
                  frameborder="0"
                  allowTransparency="true"
                  allow="encrypted-media"
                  allowFullScreen="true"
                  ></iframe></v-col>
                  <v-col><iframe
                  src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter%2Fposts%2F105065074714219&show_text=true&width=552&height=168&appId"
                  width="534"
                  height="351"
                 ></iframe></v-col><v-col>
                  <iframe
                  src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter%2Fposts%2F104160664804660&show_text=true&width=552&height=497&appId"
                  width="534"
                  height="351"
                  ></iframe></v-col>
                  </v-container>
                <v-container justify-end><NuxtLink
        to="/news"
        class="button">MORE NEWS</NuxtLink>
                </v-container>

              </section>

              <section id="events">
                                <v-container>
                  <h2
                    class="display-2 font-weight-bold mb-3 text-uppercase text-center"
                  >
                    Upcoming Events
                  </h2>

                  <v-responsive class="mx-auto mb-12" width="56">
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive>

                  <v-row>
                                         </v-row>
                </v-container>
<v-container justify-end><NuxtLink
        to="/events"
        class="button">GO TO EVENTS PAGE</NuxtLink>
                                        </v-container>
                <div class="py-12"></div>
              </section>
            </v-main>
          </v-app>
        </div>
      </body>
  </div>
</template>

<script src="https://cdn.jsdelivr.net/npm/vue@2.x/dist/vue.js"></script>
<script src="https://cdn.jsdelivr.net/npm/vuetify@2.x/dist/vuetify.js"></script>
<script>
import Vue from "vue";
import Vuetify from "vuetify";
Vue.use(Vuetify);

new Vue({
  el: "#app",
  vuetify: new Vuetify(),
  data() {
    return {
      // articles: [
      //   {
      //     src:
      //       "https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80",
      //     title: "Mobile first & Responsive",
      //     text:
      //       "Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum."
      //   },
      //   {
      //     src:
      //       "https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80",
      //     title: "Think outside the box",
      //     text:
      //       "Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh."
      //   },
      //   {
      //     src:
      //       "https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80",
      //     title: "Small changes, big difference",
      //     text:
      //       "Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget."
      //   }
      // ],
      // features: [
      //   {
      //     icon: "mdi-account-group-outline",
      //     title: "Vibrant Community",
      //     text:
      //       "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam"
      //   },
      //   {
      //     icon: "mdi-update",
      //     title: "Frequent Updates",
      //     text:
      //       "Sed ut elementum justo. Suspendisse non justo enim. Vestibulum cursus mauris dui, a luctus ex blandit. Lorem ipsum dolor sit amet consectetur adipisicing elit. qui ipsum eveniet facilis obcaecati corrupti consectetur adipisicing elit."
      //   },
      //   {
      //     icon: "mdi-shield-outline",
      //     title: "Long-term Support",
      //     text:
      //       "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam"
      //   }
      // ],
      // stats: [
      //   ["24k", "Github Stars"],
      //   ["330+", "Releases"],
      //   ["1m", "Downloads/mo"],
      //   ["5m", "Total Downloads"]
      // ]
    };
  }
});

export default {};
</script>

<style>

</style>
