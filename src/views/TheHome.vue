<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
<the-side-bar/>
<the-right-side-bar/>
<v-container>
  <v-toolbar color="rgba(0,0,0,0)" flat>
    <v-toolbar-title class="mt-n4 white--text ">Task Manager</v-toolbar-title>
  </v-toolbar>
  <v-toolbar class="mt-n6" color="rgba(0,0,0,0)" flat dark >
    <div>
      <v-icon class="mr-2" color="#7c7c7f">far fa-calendar-alt</v-icon>
      <v-badge content="2" color="red">
        <span class="caption grey--text mt-2">DES 15, 2022</span>
      </v-badge>
    </div>
    <v-spacer></v-spacer>
    <div color="rgba(0,0,0,0)" >
      <v-tabs color="#a9ddd8" right background-color="#171721">
        <v-tab >Day</v-tab>
        <v-tab >Week</v-tab>
        <v-tab >Month</v-tab>
        <v-tab >Year</v-tab>
      </v-tabs>
    </div>
  </v-toolbar>
</v-container>
  </v-app>
</template>

<script>

import TheSideBar from '@/components/TheSideBar.vue'
import TheRightSideBar from '@/components/TheRightSideBar.vue'

  export default {
    name: 'TheHome',

    components: {
    TheSideBar,
    TheRightSideBar
},
  }
</script>


<style scoped>
.theme--light.v-timeline::before{
  background: #7c7c7f;
}

.border{
  background: #22222c;
  border-radius: 50%;
}
</style>