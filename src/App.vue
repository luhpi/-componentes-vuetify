<template>
  <v-app>
    <v-container align-center>
      <v-layout row align-center>
        <v-flex xs12>
          <Home />
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
import Home from "./views/Home.vue";
export default {
  name: "App",
  data: () => ({
    //
  }),
  components: {
    Home
  }
};
</script>

<style>
img {
  max-height: 350px;
  width: auto;
}
</style>
