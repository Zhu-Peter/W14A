<template>
    <div>
        <h1>{{ edited_joke }}</h1>
    </div>
</template>
<script>
export default {
    name: 'SnakeJoke',
    props: {
        joke: String
    },
    data() {
        return {
            edited_joke: ''
        }
    },
    mounted() {
        let temp_joke = '';
        for(let i = 0; i<this.joke.length; i++){
            if(this.joke[i] == ' '){
                temp_joke = temp_joke + '-';
            }else{
                temp_joke = temp_joke + this.joke[i];
            }
        }
        this.edited_joke = temp_joke;
    },
}
</script>
<style scoped>
    
</style>