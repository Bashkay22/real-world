<script >
import { RouterLink, RouterView } from 'vue-router'

import SignUp from "./components/SignUp.vue"

export default  {

  components : {
    SignUp,
  }
}
</script>

<template>
  <header>
    

    <div class="wrapper">
      <nav>
        <SignUp />
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>


@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;

  }

  

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
   
  }
}
</style>
