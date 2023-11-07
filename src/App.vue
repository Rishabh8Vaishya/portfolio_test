<template>
  <v-app>
    <v-main>
      <!-- <HelloWorld/> -->
      <homeView />
    </v-main>
    <!-- <NavBar /> -->
  </v-app>
</template>

<script>
import HomeView from './views/HomeView.vue'
// import HelloWorld from './components/HelloWorld.vue'
// import NavBar from './components/NavBar.vue';

export default {
  name: 'App',

  components: {
    HomeView
    // HelloWorld,
    // NavBar
  },

  data: () => ({
    //
  }),
}
</script>
