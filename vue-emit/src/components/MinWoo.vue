<template>
    <div>
        <h1>{{ title }}</h1>
        <p> {{ name }}</p><br>
        <button @click='updateName'>Change Name</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            /* name: 'MinWoo', */ //props에서 name을 사용중이기 때문에 다른 곳에서는 사용 불가능 
        }
    },
    methods: {
        updateName() {
            this.name ='MinWoo updated';
        }
    },
    props: { // props로 받은 데이터를 직접적으로 변경 불가능 warn 발생 부모에서 변경하는 방법을 사용해야한다.
        title: {
            type: String,
            required: true,
            default: 'default title', 
        },
        name: {
            type: String,
            required: true,
            default: 'default name', 
        },
    },
    
}
</script>

<style scoped>

</style>