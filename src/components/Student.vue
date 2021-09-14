<template>
  <div>
  <h1 style="color:black;">Student Data</h1>
  <div style="overflow-x:auto;">
    <div v-for="item in list" v-bind:key="item.id">
      <student-card :student="item"/>
    </div>
    
    </div>
  </div>
</template>

<script >
import Vue from "vue";
import axios from "axios";
import VueAxios from "vue-axios";

import StudentCard from "./StudentCard"
Vue.use(VueAxios, axios);
export default {
  name: "student",
  data() {
    return {
      list: undefined,
    };
  },
  components:{
    StudentCard
  },
  mounted() {
    Vue.axios
      .get("https://jsonplaceholder.typicode.com/users")
      .then((response) => {
        this.list = response.data;
        console.warn(response.data);
      });
  },
};
</script>
<style >
.table {
  color: black;
  border: 1px solid black;
}
table, th, td {
  border:1px solid black;
}
h1{
  margin-top:50px;
}

</style>
