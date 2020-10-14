<template>
  <div
  >
      <head>
        <title>KS Wrestling Center</title>
        <charset="utf-8" />
        <name="viewport" content="width=device-width, initial-scale=1.0" />
        <link
          href="https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900"
          rel="stylesheet"
        />
        <link
          href="https://cdn.jsdelivr.net/npm/@mdi/font@4.x/css/materialdesignicons.min.css"
          rel="stylesheet"
        />
        <link
          href="https://cdn.jsdelivr.net/npm/vuetify@2.x/dist/vuetify.min.css"
          rel="stylesheet"
        />
        <link
          rel="shortcut icon"
          href="https://cdn.vuetifyjs.com/images/logos/favicon.ico"
        />
        <div id="fb-root"></div>
      </head>
      <body>
        <div id="app">
          <v-app>
            <v-main>
              <v-app-bar app color="black" background-opacity="50%" height="80">
                <v-avatar class="elevation-12 mr-3" size="70">
                    <v-img
                    contain
                    src="https://scontent-dfw5-2.xx.fbcdn.net/v/t1.0-9/121269031_103252158228844_7346466079413371283_o.png?_nc_cat=107&_nc_sid=09cbfe&_nc_ohc=XfSpy9JF65cAX_PxPvv&_nc_ht=scontent-dfw5-2.xx&oh=4fe2d9e8447d247e88a5178859df8fd4&oe=5FAC741E"
                    max-height="100%"
                    ></v-img>
                  </v-avatar>

                <v-toolbar-title class="white--text headline">
                KS Wrestling Center
              </v-toolbar-title>

            </v-app-bar>
            <section id="hero">
                <v-row
                  align="center"
                  justify="center"
                  >
                  <v-img
                  height="500"
                    src="https://scontent-dfw5-2.xx.fbcdn.net/v/t1.0-9/121015140_103253078228752_7405710129881532891_o.jpg?_nc_cat=104&_nc_sid=e3f864&_nc_ohc=V7hIRNO8R10AX8fR-0W&_nc_ht=scontent-dfw5-2.xx&oh=c6ac62f532eb2e8213b304400c31459e&oe=5FAB8252"
                  >
                    <v-theme-provider dark>
                      <v-container fill-height>
                        <v-row
                          align="center"
                          class="white--text mx-auto"
                          justify="center"
                        >
                          <v-col
                            class="white--text text-center"
                            cols="12"
                            tag="h1"
                          >
                            <span
                              :class="[
                                $vuetify.breakpoint.smAndDown
                                  ? 'display-2'
                                  : 'display-3'
                              ]"
                              class="font-weight-black"
                            >
                              WELCOME TO
                            </span>

                            <br />

                            <span
                              :class="[
                                $vuetify.breakpoint.smAndDown
                                  ? 'display-3'
                                  : 'display-4'
                              ]"
                              class="font-weight-black"
                            >
                              KS Wrestling Center
                            </span>
                          </v-col>

                          <v-btn
                            class="align-self-end"
                            fab
                            outlined
                            @click="$vuetify.goTo('#about-me')"
                          >
                            <v-icon>mdi-chevron-double-down</v-icon>
                          </v-btn>
                        </v-row>
                      </v-container>
                    </v-theme-provider>
                  </v-img>
                </v-row>
              </section>
              <section id="about-me">
                <div class="py-12"></div>
                  <v-container fill-height>
                        <v-row
                          align="center"
                          class="white--text mx-auto"
                          justify="center"
                        >
                          <v-col
                            class="black--text text-left"
                            cols="12"
                            tag="h1"
                          >
                            <span
                              :class="[
                                $vuetify.breakpoint.smAndDown
                                  ? 'display-1'
                                  : 'display-2'
                              ]"
                              class="font-weight-light"
                            >
                            <h2
                            class="display-2 font-weight-bold mb-3">WHO WE ARE</h2>
                  <v-responsive class="mx-auto mb-8" width="556">
                    <v-divider class="mb-1" ></v-divider><v-divider></v-divider>
                  </v-responsive>
                            </span>
                            <span
                              :class="[
                                $vuetify.breakpoint.smAndDown
                                  ? 'display-3'
                                  : 'display-4'
                              ]"
                              class="font-weight-black"
                            >
                            <v-responsive
                    class="mx-auto title font-weight-light mb-8"
                    max-width="1000"
                  >
                    KC Wrestling K.W.C. provides premium facilities for hosting Wrestling and M.M.A driven events. We provide premium venue services with a focus on innovating the user experience.
                  <br><br>
                  **20 WRESTLING MATS** is the amount of space we are talking about. We aim to drive economic growth and and enhance the quality of wrestling life by providing facilities that are safe, versatile and active. Send us a message if you wish to know more.
                  </v-responsive>
                            </span><v-responsive class="mx-auto mb-8" width="556">
                    <v-divider class="mb-1" ></v-divider><v-divider></v-divider>
                  </v-responsive>
                          </v-col>
                        </v-row>
                      </v-container>
                                </v-row>
                                <v-container class="text-center">
                                    <v-avatar class="elevation-12 mb-12" size="240">
                    <v-img
                    src="https://scontent-dfw5-2.xx.fbcdn.net/v/t1.0-9/121269031_103252158228844_7346466079413371283_o.png?_nc_cat=107&_nc_sid=09cbfe&_nc_ohc=XfSpy9JF65cAX_PxPvv&_nc_ht=scontent-dfw5-2.xx&oh=4fe2d9e8447d247e88a5178859df8fd4&oe=5FAC741E"
                    ></v-img>
                  </v-avatar>

                  <div></div>
                  <v-btn
                            class="align-self-end"
                            fab
                            outlined
                            @click="$vuetify.goTo('#hero')"
                          >
                            <v-icon>mdi-chevron-double-up</v-icon>
                          </v-btn>
                </v-container>

                <div class="py-12"></div>
              </section>

              <section id="features" class="grey lighten-3">
                <div class="py-12"></div>

                <v-container class="text-center">
                  <h2 class="display-2 font-weight-bold mb-3">
                    VUETIFY FEATURES
                  </h2>

                  <v-responsive class="mx-auto mb-12" width="56">
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive>

                  <v-row>
                    <v-col
                      v-for="({ icon, title, text }, i) in features"
                      :key="i"
                      cols="12"
                      md="4"
                    >
                      <v-card class="py-12 px-4" color="grey lighten-5" flat>
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

              <section id="stats">
                  <v-container fill-height>
                    <v-row class="mx-auto">
                      <v-col
                        v-for="[value, title] of stats"
                        :key="title"
                        cols="20"
                        md="3"
                      >
                        <div class="text-center">
                          <div
                            class="display-3 font-weight-black mb-4"
                            v-text="value"
                          ></div>

                          <div
                            class="title font-weight-regular text-uppercase"
                            v-text="title"
                          ></div>
                        </div>
                      </v-col>
                    </v-row>
                  </v-container>
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
                       <v-img
                        :src="src"
                        class="mb-4"
                        height="275"
                        max-width="100%"
                      ></v-img>

                      <h3
                        class="font-weight-black mb-4 text-uppercase"
                        v-text="title"
                      ></h3>

                      <div
                        class="title font-weight-light mb-5"
                        v-text="text"
                      ></div>

                      <v-btn class="ml-n4 font-weight-black" text>
                        Continue Reading
                      </v-btn>
                                  </v-row>
                </v-container>

                <div class="py-12"></div>
              </section>

              <v-sheet id="contact" color="#333333" dark tag="section" tile>
                <div class="py-12"></div>

                <v-container>
                  <h2
                    class="display-2 font-weight-bold mb-3 text-uppercase text-center"
                  >
                    Questions?
                    <br><br>
                    Contact Us!
                  </h2>

                  <v-responsive class="mx-auto mb-12" width="56">
                    <v-divider class="mb-1"></v-divider>

                    <v-divider></v-divider>
                  </v-responsive>

                  <v-theme-provider light>
                    <v-row>
                      <v-col cols="12">
                        <v-text-field flat label="Name*" solo></v-text-field>
                      </v-col>

                      <v-col cols="12">
                        <v-text-field flat label="Email*" solo></v-text-field>
                      </v-col>

                      <v-col cols="12">
                        <v-text-field flat label="Subject*" solo></v-text-field>
                      </v-col>

                      <v-col cols="12">
                        <v-textarea flat label="Message*" solo></v-textarea>
                      </v-col>

                      <v-col class="mx-auto" cols="auto">
                        <v-btn color="accent" x-large>
                          Submit
                        </v-btn>
                      </v-col>
                    </v-row>
                  </v-theme-provider>
                </v-container>

                <div class="py-12"></div>
              </v-sheet>
            </v-main>
            <v-footer class="justify-center" color="#292929" height="100">
              <div
                class="title font-weight-light grey--text text--lighten-1 text-center"
              >
                &copy; {{ new Date().getFullYear() }} — Vuetify, LLC — Made with
                💜 by ADI
              </div>
            </v-footer>
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
.container {
  margin: 0 auto;
  min-height: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
