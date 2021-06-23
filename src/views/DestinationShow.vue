<template>
  <section class="destination">
    <h1>{{ destination.name }}</h1> 
    <!-- destination comes from computed destination method -->
    <div class="destination-details">
      <img :src="`/images/${destination.image}`" :alt="destination.name">
      <p> {{ destination.description }} </p>
    </div>
  </section>
</template>

<script>
/* 
 * create view file
 * create route with param for that file
 * get param id. I created computed prop but you can choose anything
 * find that param id in database. In my case data.json file
 * finally bind data into template
 */

import sourceData from '../data.json';


export default {
  // 
  computed: {
    // get destination id from route param
    destinationId() {
      return parseInt(this.$route.params.id);
    },

    // find route param id in data.jason
    destination () {
      return sourceData.destinations.find( destination => destination.id === this.destinationId );
    }
  }
} 
</script>

