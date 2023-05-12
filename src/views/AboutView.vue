<template>
  

  <h1>DATA INFO</h1>
<div id="comp">
    <ul class="court" v-for="item in list" :key="item.id">
        <li>{{ item.id }}</li>
        <li>{{ item.email }}</li>
        <li>{{ item.first_name }}</li>
        <li>{{ item.last_name }}</li>
        <li><img :src="item.avatar" alt=""></li>
    </ul>
</div>
</template> 

<script>
import axios from "axios"
export default {
    name: "About",
    data() {
        return {
            list: []
        }
    },
    async mounted() {
        let result = await axios.get('https://reqres.in/api/users?page=1');
        this.list = result.data.data
    }
}
</script>

<style>
h1{
  padding-left: 2.5rem;
}
#comp{
  display: flex;
  justify-content: center;
}
.court {
  
    border: 1px solid rgb(91, 90, 90);
    padding: 1rem;
    display: inline-block;
}

li {
  display: flex;
    align-items: center;
    list-style: none;

}
</style>
