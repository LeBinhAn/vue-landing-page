<template>
  <v-app>
    <v-app-bar
      app
      color="blue lighten-5"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/5660d61c-0c05-430f-9bed-fb26c4f31707_200x200.png"
          transition="scale-transition"
          width="100"
        />
        
      </div>
      <v-spacer></v-spacer>
      <div id="gi-link">
          <h1>I made website</h1>
      </div>
    </v-app-bar>
    <v-main>
      <SearchBox/>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import SearchBox from './components/SearchBox';

export default {
  name: 'App',

  components: {
    HelloWorld,
    SearchBox
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss">
  @import './scss/main.scss';
  #gi-link {
    text-decoration: none;
    h1 {
      color: black;
      font-family: 'VT323', monospace;
      font-weight: 200;
    }
  }
  h1 {
    color: white;
  }
</style>
