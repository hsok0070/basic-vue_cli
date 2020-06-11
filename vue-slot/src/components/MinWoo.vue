<template>
    <div>
        <p>header</p>
        <slot name='header' :name1='name1'></slot>
        <p>Body</p>
        <slot></slot>
        <p>footer</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name1: 'MinWoo',
        }
    },
    methods: {
        updateName() {
            this.name ='MinWoo updated';
        }
    }
}
</script>

<style scoped>

</style>