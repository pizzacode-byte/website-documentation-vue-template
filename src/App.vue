<template>
  <dropdown-navbar></dropdown-navbar>
</template>

<script>
import dropdownNavbar from './components/navbars/dropdown-navbar.vue'
export default {
  name: 'App',
  components: {
    dropdownNavbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lato&family=Nunito+Sans&display=swap');

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
