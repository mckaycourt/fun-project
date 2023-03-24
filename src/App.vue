<template>
  <div>
    <hello-world msg="You did it!" />
    <div>{{ twoDigits }}</div>
    <stuff
        v-for="s in stuff"
        :name="capitalizeFirstLetter(s)"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Stuff from './components/Stuff.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Stuff
  },
  created () {
    this.stuff = [{
      name: 'movies',
    }, {
      name: 'books',
    }, {
      name: 'music'
    }]
  },
  computed: {
    twoDigits () {
      return this.something.toFixed(2)
    }
  },
  methods: {
    capitalizeFirstLetter ({ name }) {
      const [firstLetter] = name
      return `${firstLetter.toUpperCase()}${name.substring(1, name.length)}`
    }
  },
  data () {
    return {
      stuff: [],
      something: 1.45789847
    }
  }
}
</script>

<style scoped>
  .red-background {
    background-color: grey;
  }
</style>
