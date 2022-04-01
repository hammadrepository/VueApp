<template>
  <div class="hello px-2">
<HeaderComponent heading="App"></HeaderComponent>
<a href="#" class="flex flex-col bg-white border shadow-md md:flex-row md:max-w-xl hover:border-gray-300 dark:border-gray-700 px-4 py-2 dark:hover:bg-gray-700" v-for="products in productsData.products" v-bind:key="products[0]" v-bind:style="products.available ? ' ' : 'flex-direction :row-reverse !important;'">
    <img   class="object-cover md:h-28 md:w-36" src="../../public/image.png" alt="" >
    <div class="flex flex-col p-2 w-80">
        <h5 class="mb-2 font-bold text-left text-gray-900 dark:text-white">{{ products.name }}</h5>
        <p class="mb-1 text-left  truncate ... text-gray-700 dark:text-gray-400">{{ products.description }}</p>
        <p class="text-left text-black"><span class="font-bold">Pries:</span> {{ products.price.value}} {{ products.price.currency}}</p>
    </div>
</a>
  </div>

</template>

<script>
import HeaderComponent from './HeaderComponent.vue'
import productsJson from '/public/products.json'
export default {
  name: 'HomeComponent',
  components: {
    HeaderComponent 
  },
  data(){
        return {
          productsData : ''
        }
    },
    methods : {
      readData(){
          this.productsData = productsJson
      }
    },
    mounted(){
      this.readData();
    },
  props: {
    msg: String
  }
}
</script>

<style scoped>

</style>
