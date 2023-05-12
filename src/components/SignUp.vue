<template>
<section class="signup-view">
    <form class="ui form">
        <NameField />
    </form>
    
</section>

<section>
    <fecthInApi />
</section>
</template>
<script>
import NameField from "../components/NameField.vue"
import fecthInApi from "./fecthInApi.vue";
export default {
    components :{
        NameField,
        fecthInApi,
    }
  

}
</script>
<style>
.signup-view{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
.form{
    width: 450px;
}
</style>