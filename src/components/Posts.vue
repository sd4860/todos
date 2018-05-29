<template>
    <div>
        <p v-for="post in posts">{{ post.title }}</p>
    </div>    
</template>

<script>
import axios from 'axios';

export default {
    name: 'Posts',
    data() {
        return {
            posts: []
        }
    },
    mounted() {
        axios.get('https://jsonplaceholder.typicode.com/posts')
            .then(response => {
                console.log(response.data);
                this.posts = response.data;
            })
    }
}
</script>

<style>

</style>
