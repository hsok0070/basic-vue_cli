<template>
  <div class="mb-2 d-flex">
      <div>
        <input type="checkbox" 
        :checked="todo.checked"
        @change="toggleCheckbox"
        >
      </div>
      <span 
          class="ml-3 flex-grow-1"
          :class="todo.checked ? 'text-muted' : ''"
          :style="todo.checked ? 'text-decoration: line-through': ''"
      > 
      {{ todo.text }}
      </span>
      <button 
        class='btn btn-danger btn-sm'
        @click="clickDelete"
      >Delete</button>
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
            });
        },
        clickDelete() {
            this.$emit('click-delete', this.todo.id)
        }
    }
}
</script>

<style>

</style>