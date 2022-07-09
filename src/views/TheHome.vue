<template>
  <v-app :style="{ background: $vuetify.theme.themes.dark.background }">
    <the-side-bar />
    <the-right-side-bar />
    <v-container>
      <v-toolbar color="rgba(0,0,0,0)" flat>
        <v-toolbar-title class="mt-n4 white--text ">Task Manager</v-toolbar-title>
      </v-toolbar>
      <v-toolbar class="mt-n6" color="rgba(0,0,0,0)" flat dark>
        <div>
          <v-icon class="mr-2" color="#7c7c7f">far fa-calendar-alt</v-icon>
          <v-badge content="2" color="red">
            <span class="caption grey--text mt-2">DES 15, 2022</span>
          </v-badge>
        </div>
        <v-spacer></v-spacer>
        <div color="rgba(0,0,0,0)">
          <v-tabs color="#a9ddd8" right background-color="#171721">
            <v-tab>Day</v-tab>
            <v-tab>Week</v-tab>
            <v-tab>Month</v-tab>
            <v-tab>Year</v-tab>
          </v-tabs>
        </div>
      </v-toolbar>
      <v-divider color="#7c7c7f"> </v-divider>
      <v-row>
        <v-col cols="12" sm="3">
          <v-list class=" mt-3" rounded flat color="rgba(0,0,0,0)">
            <v-list-item-group v-model="selectItem" color="#a9ddd8">
              <v-list-item active-class="border">
                <v-list-item-content>
                  <v-list-item-title class="grey--text">Design</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
              <v-list-item class=" mt-11" active-class="border">
                <v-list-item-content>
                  <v-list-item-title class="grey--text">Mobile App</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
              <v-list-item class=" mt-8" active-class="border">
                <v-list-item-content>
                  <v-list-item-title class="grey--text">Infography</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
              <v-list-item class=" mt-8" active-class="border">
                <v-list-item-content>
                  <v-list-item-title class="grey--text">Prototyping</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-col>
        <v-col cols="12" sm="9">
          <v-timeline class=" mt-2 mr-3" align-top :dense="$vuetify.breakpoint.smAndDown">
            <v-timeline-item color="red" fill-dot small>
              <v-card color="#22222c" dark>
                <v-card-title class=" text-subtitle-2 red--text">
                  About 2 hours
                  <v-spacer></v-spacer>
                  <v-avatar size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/4.jpg" alt="alt">
                  </v-avatar>
                  <v-avatar class=" ml-n3" size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/5.jpg" alt="alt">
                  </v-avatar>
                </v-card-title>
              </v-card>
            </v-timeline-item>
            <v-timeline-item color="light-blue" fill-dot small>
              <v-card color="#22222c" dark>
                <v-card-title class=" text-subtitle-2 light-blue--text">
                  About 30 mines
                  <v-spacer></v-spacer>
                  <v-avatar size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/2.jpg" alt="alt">
                  </v-avatar>
                  <v-avatar class=" ml-n3" size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/3.jpg" alt="alt">
                  </v-avatar>
                </v-card-title>
              </v-card>
            </v-timeline-item>
            <v-timeline-item color="pink" fill-dot small>
              <v-card color="#22222c" dark>
                <v-card-title class=" text-subtitle-2 pink--text">
                  About 3 hours
                  <v-spacer></v-spacer>
                  <v-avatar size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/4.jpg" alt="alt">
                  </v-avatar>
                  <v-avatar class=" ml-n3" size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/1.jpg" alt="alt">
                  </v-avatar>
                </v-card-title>
              </v-card>
            </v-timeline-item>
            <v-timeline-item color="amber" fill-dot small>
              <v-card color="#22222c" dark>
                <v-card-title class=" text-subtitle-2 amber-blue--text">
                  About 50 mines
                  <v-spacer></v-spacer>
                  <v-avatar size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/5.jpg" alt="alt">
                  </v-avatar>
                  <v-avatar class=" ml-n3" size="30">
                    <img src="http://cdn.vuetifyjs.com/images/lists/3.jpg" alt="alt">
                  </v-avatar>
                </v-card-title>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="4">
          <v-card class=" rounded-lg " elevation="10" color="#22222c">
            <v-app-bar color="rgba(0,0,0,0)" flat>
              <v-toolbar-title class=" pl-0 text-subtitle-2 white--text">
                UX | UI Design <br>
                <span class=" caption grey--text">Mike Creative</span>
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-btn icon small color="#7c7c7f">
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </v-app-bar>
            <v-app-bar class="mt-n7" flat color="rgba(0,0,0,0)">
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/4.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/5.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/2.jpg" alt="alt">
              </v-avatar>
            </v-app-bar>
            <v-app-bar class="mt-n6" flat color="rgba(0,0,0,0)">
              <span class=" grey--text " small> Progress</span>
              <v-spacer></v-spacer>
              <span class=" grey--text caption">50%</span>
            </v-app-bar>
            <v-app-bar class="mt-n10" flat color="rgba(0,0,0,0)" >
              <v-progress-linear color="green" value="50" height="6" ></v-progress-linear>
            </v-app-bar>
            <v-card-text class=" pt-0">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-icon class=" mr-2" color="#7c7c7f" small>fas fa-share-alt</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">8</span>
                  <v-icon class=" ml-2 mr-2" small color="#7c7c7f">far fa-comment-dots</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">2</span>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-chip dark color="#7c7c7f" small>
                    <v-icon small left>mdi-alarm-check</v-icon>
                    3 week
                  </v-chip>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4">
          <v-card class=" rounded-lg " elevation="10" color="#22222c">
            <v-app-bar color="rgba(0,0,0,0)" flat>
              <v-toolbar-title class=" pl-0 text-subtitle-2 white--text">
                QA Dev <br>
                <span class=" caption grey--text">QA Development</span>
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-btn icon small color="#7c7c7f">
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </v-app-bar>
            <v-app-bar class="mt-n7" flat color="rgba(0,0,0,0)">
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/1.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/4.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/5.jpg" alt="alt">
              </v-avatar>
            </v-app-bar>
            <v-app-bar class="mt-n6" flat color="rgba(0,0,0,0)">
              <span class=" grey--text " small> Progress</span>
              <v-spacer></v-spacer>
              <span class=" grey--text caption">40%</span>
            </v-app-bar>
            <v-app-bar class="mt-n10" flat color="rgba(0,0,0,0)" >
              <v-progress-linear color="green" value="40" height="6" ></v-progress-linear>
            </v-app-bar>
            <v-card-text class=" pt-0">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-icon class=" mr-2" color="#7c7c7f" small>fas fa-share-alt</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">3</span>
                  <v-icon class=" ml-2 mr-2" small color="#7c7c7f">far fa-comment-dots</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">4</span>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-chip dark color="#7c7c7f" small>
                    <v-icon small left>mdi-alarm-check</v-icon>
                    7 week
                  </v-chip>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4">
          <v-card class=" rounded-lg " elevation="10" color="#22222c">
            <v-app-bar color="rgba(0,0,0,0)" flat>
              <v-toolbar-title class=" pl-0 text-subtitle-2 white--text">
                Front-End Development<br>
                <span class=" caption grey--text">Vue Halper</span>
              </v-toolbar-title>
              <v-spacer></v-spacer>
              <v-btn icon small color="#7c7c7f">
                <v-icon>mdi-dots-vertical</v-icon>
              </v-btn>
            </v-app-bar>
            <v-app-bar class="mt-n7" flat color="rgba(0,0,0,0)">
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/2.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/4.jpg" alt="alt">
              </v-avatar>
              <v-avatar class=" ml-n3" size="30">
                <img src="http://cdn.vuetifyjs.com/images/lists/1.jpg" alt="alt">
              </v-avatar>
            </v-app-bar>
            <v-app-bar class="mt-n6" flat color="rgba(0,0,0,0)">
              <span class=" grey--text " small> Progress</span>
              <v-spacer></v-spacer>
              <span class=" grey--text caption">5%</span>
            </v-app-bar>
            <v-app-bar class="mt-n10" flat color="rgba(0,0,0,0)" >
              <v-progress-linear color="green" value="5" height="6" ></v-progress-linear>
            </v-app-bar>
            <v-card-text class=" pt-0">
              <v-row>
                <v-col cols="12" sm="8">
                  <v-icon class=" mr-2" color="#7c7c7f" small>fas fa-share-alt</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">3</span>
                  <v-icon class=" ml-2 mr-2" small color="#7c7c7f">far fa-comment-dots</v-icon>
                  <span class=" text-caption  grey--text  font-weight-light">7</span>
                </v-col>
                <v-col cols="12" sm="4">
                  <v-chip dark color="#7c7c7f" small>
                    <v-icon small left>mdi-alarm-check</v-icon>
                    5 week
                  </v-chip>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>

import TheSideBar from '@/components/TheSideBar.vue'
import TheRightSideBar from '@/components/TheRightSideBar.vue'

export default {
  data: () => ({
    selectItem: 2,
  }),
  name: 'TheHome',

  components: {
    TheSideBar,
    TheRightSideBar
  },
}
</script>


<style scoped>
.theme--light.v-timeline::before {
  background: #7c7c7f;
}

.border {
  background: #22222c;
  border-radius: 50%;
}
</style>