<template>
  <div>
    <v-list-item>
      <v-list-item-content class="pl-3 py-2">
        <v-list-item-title class="title"> Navigation bar </v-list-item-title>

        <v-list-item-subtitle> This is a navigation bar </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list dense nav>
      <v-list-group v-for="category in categories" :key="category.title">
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="category.title" class="category-title">
            </v-list-item-title>
          </v-list-item-content>
        </template>

        <v-list-item
          v-for="subCategory in category.subCategories"
          :key="subCategory.title"
        >
          <v-item-content>
            <v-item-title class="sub-category-title">
              {{ subCategory.title }}
            </v-item-title>
          </v-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
  </div>
</template>
<script>
export default {
  name: "NavigationData",
  data: () => ({
    categories: [],
  }),
  watch: {
    group() {
      this.drawer = false;
    },
  },
  mounted() {
    this.getCategories();
  },
  methods: {
    getCategories: function () {
      let self = this;
      let axios = require("axios");
      axios
        .get("http://localhost:8080/api.exampleproject.gisoft/categories")
        .then((response) => {
          return (self.categories = response.data.data);
        })
        .catch((e) => console.log(e));
    },
  },
};
</script>
<style lang=""></style>
