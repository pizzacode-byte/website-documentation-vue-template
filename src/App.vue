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
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
