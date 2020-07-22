<template>
  <div>
    <ul class="" v-for="user in usersList" :key="user.id">
      <li class="">
        <strong>Name: {{ user.name }}</strong> <br><br>
        <div class="">Email: {{ user.email }}</div> <br>
        <div>Website: {{ user.website }}</div>
      </li>
    </ul>
  </div>
</template>

<script>
// import axios
import axios from "axios";

export default {
  data() {
    return {
      usersList: []
    };
  },
  mounted() {
    axios.get("https://jsonplaceholder.typicode.com/users")
      .then(res => {
        this.usersList = res.data;
        console.log(this.usersList)
      })
      .catch(error => {
        console.log(error)
         // Manage errors if found any
      })
  }
};
</script>

<style>
ul {
  margin: 0 auto;
  width: 300px;
  text-align: left;  
}

li {
  display: block;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  padding: 15px;
}
</style>