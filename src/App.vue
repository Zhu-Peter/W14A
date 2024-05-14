<template>
  <div id="app">
    <div id="button_container">
      <JokeButton />
      <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>Normal</option>
        <option>Snake</option>
        <option>Loud</option>
      </select>
    </div>
    <div id="joke_container">
      <SnakeJoke v-if="selected == 'Normal'" />
      <NormalJoke v-if="selected == 'Snake'" />
      <LoudJoke v-if="selected == 'Loud'" />
    </div>
  </div>
</template>

<script>
import JokeButton from './components/JokeButton.vue';
import SnakeJoke from './components/SnakeJoke.vue';
import NormalJoke from './components/NormalJoke.vue';
import LoudJoke from './components/LoudJoke.vue';

export default {
  name: 'App',
  components: {
    JokeButton, SnakeJoke, NormalJoke, LoudJoke
  },
  data() {
    return {
      selected: '',
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#button_container {
  display: flex;
  gap: 150px;
  margin-left: 100px;
}
</style>
