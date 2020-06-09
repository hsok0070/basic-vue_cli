<template>
    <div>
        <label for="">Name : </label>
        <input 
        type="text" 
        :value="value"
        style="padding: 5px; border: 2px solid green;"
        @input="$emit('input', $event.target.value)" 
        ><br>
        <!-- 기존 @input="updateName"를 간단하게 사용 하는방법 updateName 메소드를 만들지 않고 @input에 바로 $emit 가능 -->
    </div>
</template>

<script>
export default {
    data () {
        return {

        }
    },
    /* props: {
        name: {
            type: String,
            require: true,
            default: 'defualt name',
        }
    }, */
    props: { // 부모컴포넌트에서 v-model을 사용하여 보낼때
        value: {
            type: String,
            require: true,
            default: 'defualt name',
        }
    },
    /* methods: {
        updateName(e) {
            console.log(e.target.value);
            this.$emit('update-name', e.target.value)
        }
    } */
}
</script>