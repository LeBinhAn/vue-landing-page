<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
     
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>BinhAnDev</v-toolbar-title>
      <SearchBox/>
    </v-app-bar>

    <v-main>
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
    SearchBox,
  },
  data: () => ({ drawer: null }),
};
</script>
<style lang="scss">
  @import './scss/main.scss';
  
  h1 {
    color: white;
  }
</style>
