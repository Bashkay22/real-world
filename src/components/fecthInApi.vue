<template>
<!-- <button @click="getPosts">show Post</button> -->
<br>
<div v-for="p in post" :key="p.id">
    <h2> {{ p.id }} - {{ p.title }}</h2>
    <p>{{ p.body }}</p>
</div>
</template>


<script>
export default {
    data() {
        return {
            post: []
        }

    },
    methods: {
        getPosts() {
            fetch('https://jsonplaceholder.typicode.com/posts')
                .then(response => response.json())
                .then(data => this.post = data)
        }
    },
    mounted() {
        this.getPosts()
    }
}
</script>

<style>

</style>
