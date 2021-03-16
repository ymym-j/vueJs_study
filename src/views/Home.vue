<template>
  <div>
    <h1>Welcome to {{title}}!</h1>
    <input type="text" v-model="input1" />
    <button type="button" @click="getData()">Get</button>
    <button type="button" @click="setData()">Set</button>

    <select class="form-control" v-model="region" @change="changeRegion">
      <option :key="i" :value="d.v" v-for="(d, i) in options">{{d.t}}</option>
    </select>
    <!-- v if : false시 랜더링 x
         v show : false시 랜더링 후 숨김 -->
    <table class="table table-bordered" v-if="tableShow">
      <tr :key="i" v-for="(d, i) in options">
        <td>{{d.v}}</td>
        <td>{{d.t}}</td>
      </tr>
    </table>
  </div>
</template>


<script>
export default {
  data(){
    return {
      title: "뷰 스터디 ",
      title2: "ym",
      input1: "input data",
      options:[
        {v:"S",t:"Seoul"},
        {v:"J",t:"Jeju"},
        {v:"B",t:"Busan"},
      ],
      region: "J",
      tableShow: true,
    };
  },
  methods:{
    getData() {
      alert(this.input1);
    },
    setData() {
      this.input1="setData";
    },
    changeRegion(){
      alert(this.region);
    },
  },
  watch:{
    input1(){
      console.log(this.input1);
    },
    title(){

    }
  }
};
</script>

<style scoped>

</style>