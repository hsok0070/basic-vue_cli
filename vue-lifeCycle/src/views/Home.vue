<template>
  <div class="home">
    <h1>This is Home page</h1>
    <MinWoo></MinWoo>
    <InputField :name='name'></InputField>
    <br><button @click="updateName">Submit</button>
    {{name}}
  </div>
</template>

<script>
import MinWoo from '@/components/MinWoo.vue'
import InputField from '@/components/InputField.vue'

export default {
  data () {
    return {
      name: 'MinWoo',
    }
  },
  components: {
    MinWoo,
    InputField,
  },
  methods: {
    updateName() {
     this.name = 'hello';
    }
  },
  beforeCreate() { //vue 인스턴스가 생성되기 전 
    console.log('beforeCreate');
  },
  created () { //vue 인스턴스가 생성된 후
    console.log('created');
  },
  beforeMount() { //dom이 마운트 되기 전
    alert('beforeMount');
  },
  mounted() { //dom이 마운트 된 후
    alert('mounted')
  },
  beforeUpdate() { // methods가 실행되기 전 
    alert('beforeUpdate')
  },
  updated() { //methods가 실행 된 후 
    alert('updated')
    },
  beforeDestroy() { // 해당 컴포넌트가 없어지기 전
    alert('beforeDestroy')
  },
  destroyed() { // 해당 컴포넌트가 없어진 후
    alert('destroyed')
  },
}
</script>

<style scoped>
h1 {
  color: red;
}
</style>