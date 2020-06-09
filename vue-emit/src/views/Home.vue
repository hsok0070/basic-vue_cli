<template>
  <div class="home">
    <h1>This is Home page</h1>
    <form action="">
      <!-- <InputField :name='name' @update-name='name = $event.target.value'></InputField> -->
      <!-- 기존 @update-name='updateNmae'를 간단하게 작성하는 방법 updateName 메소드를 만들지 않고 자식컴포넌트에서 보낸 이벤트를
      InputField 안에서 $event 를 사용하기 -->
      <InputField v-model="name"></InputField> <!-- 컴포넌트에서 v-model 사용 가능! 자식컴포넌트에 value값을 보낸다.-->
      <br><button>Submit</button> 
      <br>
    </form>
    {{ name }}
  </div>
</template>

<script>
import InputField from '@/components/InputField.vue'

export default {
  data () {
    return {
      name:'',
    }
  },
  components: {
    InputField,
  },
  /* methods: {
    updateName(name) {
      this.name = name;
    }
  } */
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>