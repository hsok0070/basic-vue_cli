<template>
    <div>
        <p>header</p>
        <slot></slot>
        <p>Body</p>
        <slot></slot>
        <p>footer</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: 'MinWoo',
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