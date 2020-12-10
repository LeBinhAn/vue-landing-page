<template>
  <v-tool-bar>
    <v-text-field
        class="mx-2"
        label="Search"
        placeholder="Search for something?"
        solo
        hide-details=""
      ></v-text-field>
  </v-tool-bar>
</template>
<script>
export default {
  name: "SearchBox",
  data: function() {
   
  },
  mounted() {
    
  },
};
</script>
<style lang="scss">
  .v-input {
    margin-top: 1em;
  }
</style>
