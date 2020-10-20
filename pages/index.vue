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

                  <v-responsive class="mx-auto mb-12" width="56">
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive>
                  <v-btn class="ml-n4 font-weight-black" text>
                        Continue Reading
                      </v-btn>

                  <v-row>
                    <v-col
                      v-for="({ icon, title, text }, i) in features"
                      :key="i"
                      cols="12"
                      md="4"
                    >
                      <v-card class="py-12 px-4" flat>
                        <v-theme-provider dark>
                          <div>
                            <v-avatar color="primary" size="88">
                              <v-icon large v-text="icon"></v-icon>
                            </v-avatar>
                          </div>
                        </v-theme-provider>

                        <v-card-title
                          class="justify-center font-weight-black text-uppercase"
                          v-text="title"
                        ></v-card-title>

                        <v-card-text class="subtitle-1" v-text="text">
                        </v-card-text>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-container>

                <div class="py-12"></div>
              </section>

              <section id="blog">
                <div class="py-12"></div>

                <v-container>
                  <h2
                    class="display-2 font-weight-bold mb-3 text-uppercase text-center"
                  >
                    Blog
                  </h2>

                  <v-responsive class="mx-auto mb-12" width="56">
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive>

                  <v-row>
                  <iframe
                    src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FksWrestlingCenter&tabs=timeline&width=500&height=500&small_header=true&adapt_container_width=true&hide_cover=true&show_facepile=true&appId"
                    width="500"
                    height="700"
                    style="border:none;overflow:hidden"
                    scrolling="no"
                    frameborder="0"
                    allowTransparency="true"
                    allow="encrypted-media">
                    </iframe>
                       </v-row>
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
