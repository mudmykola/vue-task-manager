<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
<the-side-bar/>
<the-right-side-bar/>
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
