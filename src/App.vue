<!-- <script>import Header from './components/Header.vue';</script> -->

<template>
  <v-app>
    <v-main>
      <Header></header>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',

  components: {
    Header,
  },

  data: () => ({
    //
  }),
}
</script>
