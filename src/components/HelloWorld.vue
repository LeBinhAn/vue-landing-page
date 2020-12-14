<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to My-Vue
        </h1>
        <p class="subheading font-weight-regular"></p>
      </v-col>
			<v-col cols="12">
        <div 
					v-for="product in products" 
					:key="product.name"
				>
          <div class="">
            <h4 class="">{{ product.name }}</h4>
            <p class="">{{ product.description }}</p>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
		products: []
	}),
  mounted() {
    this.getProducts();
  },
  methods: {
    getProducts: function() {
			let axios = require("axios");
      axios
        .get("http://localhost:8080/api.exampleproject.gisoft/products")
        .then((response) => {
          this.products = response.data.data;
        })
        .catch(
					(error) => console.log(error)
        );
    },
  },
};
</script>
<style lang="scss">

</style>
