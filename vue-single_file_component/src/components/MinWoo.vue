<template>
    <div>
        <p> {{ name }}</p><br>
        <button @click='updateName'>Change Name</button>
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