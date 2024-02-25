<script>
  export default {
    data(){
      return {
        increment_counter: 0,
      }
    },

    methods: {
      incrementMe(){
        this.increment_counter += 1
      }
    },
  }
</script>

<template>
  <div id="app">


    <!-- Simple Counter -->
    <p>Increment: {{ increment_counter }}</p>
    <button @click="incrementMe"> Increment </button>

  </div>
</template>