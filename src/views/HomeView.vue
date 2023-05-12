<template>
<main>
  <input type="text" v-model="search">
  <p>{{ search }}</p>
    <p v-for="name in matching" key="name">{{ name }}</p>
   
</main>
</template>

<script>
import {
    ref,
    computed,
} from 'vue';
export default {

  name:"Home",
  setup(){
    const names = ref(["Kaycee", "Kaima", "Work", "Jude", "Sebastian"])
        const search = ref('')

        const matching = computed(()=>{
          return names.value.filter((name)=> name.includes(search.value))
        })
            return {
                names,
                search,
                matching
            }
  }
}
</script>

<style>

</style>
