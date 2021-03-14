<template>
  <div>
    <h1>Welcome to {{title}}!</h1>
    <input type="text" v-model="input1" />
    <button type="button" @click="getData()">Get</button>
    <button type="button" @click="setData()">Set</button>
  </div>
</template>


<script>
export default {
  data(){
    return{
      title: "뷰 스터디 ",
      title2: "ym",
      input1: "input data"
    };
  },
  methods:{
    getData() {
      alert(this.input1);
    },
    setData() {
      this.input1="setData";
    }
  }
}
</script>

<style scoped>

</style>