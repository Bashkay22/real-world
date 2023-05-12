<template>
<div class="field">
    <div >
        
        <input type="text" placeholder="Full Name" autocomplete="off" v-model="input" @keyup="validateInput()"  >
    </div>
    <div class="jay" v-if="error">
    {{ error }}
    </div>

</div>
</template>

<script>
import {ref,computed} from 'vue';

export default {
    setup() {
        let input = ref("");
        let error = ref("");
        const validateInput = ()  => {
            error.value = input.value === "" ? "The Input field is required" : "";
        };
        return {
            input,
            error,
            validateInput,
        };
    }

};
</script>

<style>
.jay{
    color: red;
}
</style>
