<template>
  <div>
      {{ todo.checked}}
      <input type="checkbox" :checked="todo.checked">
      <span class="ml-3"> {{ todo.text }}</span>
  </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    props: {
        todo: {
            type: Object,
            required: true,
            default: 'default text',
        }
    }
}
</script>

<style>

</style>