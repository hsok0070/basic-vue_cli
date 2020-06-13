<template>
  <div>
      {{ todo.checked}}
      <input type="checkbox" 
      :checked="todo.checked"
      @change="toggleCheckbox"
      >
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
    },
    methods: {
        toggleCheckbox(e) {
            this.$emit('toggle-checkbox', {
                id: this.todo.id,
                checked: e.target.checked
            })
        }
    }
}
</script>

<style>

</style>