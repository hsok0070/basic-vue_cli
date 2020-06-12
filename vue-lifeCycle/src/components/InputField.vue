<template>
    <div>
        <label for="">Name : </label>
        <input 
        type="text" 
        style="padding:5px; border:2px solid green;"
        v-model='name'
        >
    </div>
</template>

<script>
export default {
    data() {
        return {
        
        }
    },
    props: {
        name: {
            type: String,
            required: true,
            default: 'default name',
        }
    },
}
</script>