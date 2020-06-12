<template>
  <div class="about">
    <h1>This is an about page</h1>
    <MinWoo>
      <template #header='props'> <!-- v-slot은 #으로 줄여서 사용 가능 -->
        <div>
          <p>header11 {{ props.name1 }}</p>
          {{ props.name1 }}
        </div>
      </template>
      <template v-solt:default>
        <div>
          hello1
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