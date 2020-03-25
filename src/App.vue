<template>
  <div id="app">
    <harmony-top/>
    <harmony-nav/>
    <harmony-form/>
  </div>
</template>

<script>
import harmonyForm from './views/harmonyForm'
import harmonyTop from './components/harmonyTop'
import harmonyNav from './components/harmonyNav'

export default {
  name: 'App',
  components: {
    harmonyForm,
    harmonyTop,
    harmonyNav,
  }
}
</script>

<style>
</style>
