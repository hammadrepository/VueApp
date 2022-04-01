<template>
	<div class="text-center text-lg h-10 bg-blue-500 text-white">
        <h3 class="font-bold mt-2 text-white pt-1">{{ heading }}</h3>
      </div>  
</template>

<script>

export default {
  name: 'HeaderComponent',
    data(){
        return {
        }
    },
  props: {
    heading: String
  }
}
</script>

<style scoped>

</style>
