<template>
    <div>
        <h1>{{ joke }}</h1>
    </div>
</template>
<script>
export default {
    name: 'LoudJoke',
    props: {
        joke: String
    },
}
</script>
<style scoped>
h1{
    text-transform: uppercase;
}
</style>