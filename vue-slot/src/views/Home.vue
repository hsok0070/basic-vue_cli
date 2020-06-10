<template>
  <div class="home">
    <h1>This is Home page</h1>
    <MinWoo></MinWoo>
  </div>
</template>

<script>
import MinWoo from '@/components/MinWoo.vue'

export default {
  data () {
    return {
      
    }
  },
  components: {
    MinWoo,
  }
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>