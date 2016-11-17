<template>
  <div id='app'>
    <h1>Hello World!</h1>
    <ExampleComponent/>
  </div>
</template>

<script>
  import ExampleComponent from './components/ExampleComponent.vue'

  export default {
    name: 'app',
    components: {
      ExampleComponent
    },
    mounted() {
      this.$router.push('/')
    },
    methods: {
      goHome() {
        this.$router.push('/')
      }
    }
  }

</script>

<style>
  #app {
    font-family: 'Open Sans', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #000;
    font-size: 2vw;
    padding: 5vh 5vw;
  }

  h1 {
    font-size: 4vw;
    margin-bottom: 4vh;
  }

  @media screen and (max-width: 800px) {
    #app {
      font-size: 16px;
    }

    h1 {
      font-size: 30px;
    }
  }

  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s
  }

  .fade-enter, .fade-leave-active {
    opacity: 0
  }

</style>
