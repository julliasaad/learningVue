<template>
  <div id="app">
    <h3>{{title}}</h3>
    <div class="container">
      <div class="row">
          <Character v-for="(id, index) in initial_ids" v-bind:id="id" key="index"></Character>
      </div>
    </div>
  </div>
</template>

<script>
import Character from './components/Character.vue'

export default {
  name: 'app',
  data() {
    return {
      title: 'Generate Your Team',
      initial_ids: [1, 13, 14]
    }
  },
  components: {
    Character
  }
}
</script>
