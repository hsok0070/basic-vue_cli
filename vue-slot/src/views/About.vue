<template>
  <div class="about">
    <h1>This is an about page</h1>
    <MinWoo>
      <template v-slot:header>
        <div>
          <p>header11</p>
        </div>
      </template>
    </MinWoo>
  </div>
</template>

<script>
import MinWoo from '@/components/MinWoo.vue'

export default {
  data() {
    return {

    }
  },
  components: {
    MinWoo,
  }
}
</script>