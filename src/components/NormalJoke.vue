<template>
    <div>
        <h1>{{ joke }}</h1>
    </div>
</template>
<script>
export default {
    name: 'NormalJoke',
    props: {
        joke: String
    },
}
</script>
<style scoped>
    
</style>