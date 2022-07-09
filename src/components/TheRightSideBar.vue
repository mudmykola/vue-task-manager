<template>
  <v-navigation-drawer app color="#14141c" right width="250">
    <v-toolbar color="rgba(0,0,0,0)" flat>
      <v-icon class=" mr-4" color="#7c7c7f">fas fa-search</v-icon>
      <v-badge class="mr-8" overlap bordered color="red" dot>
        <v-icon color="#7c7c7f">far fa-bell</v-icon>
      </v-badge>
      <v-divider vertical inset color="#7c7c7f"></v-divider>
      <v-spacer></v-spacer>
      <v-badge bordered bottom color="#49d9a0" dot offset-x="10" offset-y="10">
        <v-avatar class=" ml-n3" size="30">
          <v-img src="../assets/image-2.png"></v-img>
        </v-avatar>
      </v-badge>
      <v-btn text color="#7c7c7f">Linda</v-btn>
      <v-btn class=" ml-n3" icon dark>
        <v-icon x-small color="#7c7c7f">fas fa-chevron-down</v-icon>
      </v-btn>
    </v-toolbar>
    <strong class="ml-3 white--text">Overall Progress</strong><br>
    <strong class=" ml-3 grey--text caption">Pet Project</strong>
    <div class="mt-5 mb-5 text-center">
      <v-progress-circular class="mt-5 font-weight-bold" :size="100" :width="12" :value="65" color="orange darken-2" fo>65%</v-progress-circular>
    </div>
    <strong class="ml-3 white--text">Recent Activites</strong><br>
    <strong class=" ml-3 grey--text caption">07 June 2022</strong>
    <v-list three-line>
      <v-list-item-group>
        <template v-for="(item) in files">
          <v-list-item :key="item.title">
            <v-list-item-avatar>
              <img :src="item.avatar" />
            </v-list-item-avatar>
            <template>
              <v-list-item-content>
                <v-list-item-title class="white--text" v-html="item.title"></v-list-item-title>
                <v-list-item-subtitle class=" grey--text" v-text="item.subtitle"></v-list-item-subtitle>
                <v-list-item-subtitle class=" grey--text" v-text="item.time"></v-list-item-subtitle>
              </v-list-item-content>
            </template>
          </v-list-item>
        </template>
      </v-list-item-group>
    </v-list>
    <v-row>
      <v-col cols="12" sm="6">
        <v-card class=" d-flex align-center ml-4" height="60px" width="120px" color="#21212b">
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item class="text-center" two-line>
                <v-list-item-content>
                  <v-list-item-title class=" white--text">152</v-list-item-title>
                  <v-list-item-subtitle  class="grey--text caption mt-2" >Total Progress</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card class=" d-flex align-center mx-2" height="60px" width="120px" color="#a9ddd8">
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item class="text-center" two-line>
                <v-list-item-content>
                  <v-list-item-title class=" black--text ">300</v-list-item-title>
                  <v-list-item-subtitle  class="black--text caption mt-2" >Upcomping</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
       <v-col cols="12" sm="6">
        <v-card class=" d-flex align-center ml-4" height="60px" width="120px" color="#21212b">
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item class="text-center" two-line>
                <v-list-item-content>
                  <v-list-item-title class=" white--text">200</v-list-item-title>
                  <v-list-item-subtitle  class="grey--text caption mt-2" >In Progress</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6">
        <v-card class=" d-flex align-center mx-2" height="60px" width="120px" color="#21212b">
          <v-row>
            <v-col cols="12" sm="12">
              <v-list-item class="text-center" two-line>
                <v-list-item-content>
                  <v-list-item-title class=" white--text ">452</v-list-item-title>
                  <v-list-item-subtitle  class="grey--text caption mt-2" >Complete</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    files: [
      {
        avatar: 'http://cdn.vuetifyjs.com/images/lists/1.jpg',
        time: '2 Mins Ago',
        subtitle: 'QA Automatic',
        title: '<strong>Miki Roi  </strong>',
      },
      {
        avatar: "http://cdn.vuetifyjs.com/images/lists/5.jpg",
        time: '10 Mins Ago',
        subtitle: 'Backand Developer',
        title: '<strong>Simo Muore </strong>',
      },
      {
        avatar: 'http://cdn.vuetifyjs.com/images/lists/3.jpg',
        time: '20 Mins Ago',
        subtitle: 'Front End Developer',
        title: '<strong>Sab Zirot </strong>',
      },


    ]
  })
}
</script>

<style>
</style>