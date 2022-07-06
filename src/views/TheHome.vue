<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
<the-side-bar/>
  </v-app>
</template>

<script>

import TheSideBar from '@/components/TheSideBar.vue'

  export default {
    name: 'TheHome',

    components: {
    
    TheSideBar
},
  }
</script>
