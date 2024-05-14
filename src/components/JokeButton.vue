<template>
    <div>
        <button @click="getJoke">Get Joke</button>
    </div>
</template>
<script>
import axios from "axios";

export default {
    name: 'JokeButton',
    data() {
        return {
        }
    },
    methods: {
        getJoke: function () {
                axios.request({
                    url: 'https://ron-swanson-quotes.herokuapp.com/v2/quotes'
                }).then((response)=>{this.$root.$emit('jokeListener', response.data[0]); this.isJoke = true}).catch((error)=>{console.log(error)})
            
        }
    },
}
</script>
<style scoped>
    
</style>