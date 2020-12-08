<template>
  <v-app>
    <v-app-bar
      app
      color="red lighten-5"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://gisoft.vn/images/gi-icon.png"
          transition="scale-transition"
          width="50"
        />
        <a href="http://" id="gi-link">
          <h1>GI Software</h1>
        </a>
      </div>

      <v-spacer></v-spacer>
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
<style lang="sass">
  @import './styles/main.sass'
</style>
