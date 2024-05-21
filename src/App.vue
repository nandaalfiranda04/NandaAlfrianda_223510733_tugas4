<template>
  <div id="app">
    <ParentComponent />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent
  }
};
</script>

<style>
/* Global Styles */
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f4;
  color: #333;
}

#app {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}
</style>
