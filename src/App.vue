<template>
<div>
  <LikeHeader></LikeHeader>
  <p>{{ number }}</p>
  <LikeNumber :total-number="number" v-on:my-click="incrementNumber"></LikeNumber>
  
  <LikeNumber :total-number="number"></LikeNumber>
 </div>

</template>

<script>

import LikeHeader from "./components/LikeHeader.vue";
export default {
  data() {
   return {
    number: 100
   };
  },
  components: {
    LikeHeader
  },
  methods: {
    incrementNumber(value) {
      this.number = value;
    }
  }
}
</script>


<style scoped>
  div  {
    border: 1px solid blue;
  }

</style>