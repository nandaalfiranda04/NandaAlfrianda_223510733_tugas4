<template>
    <div class="child">
      <h2>Pilih Kelompok</h2>
      <slot></slot>
      <GrandChildComponent @send-data="forwardData"></GrandChildComponent>
    </div>
  </template>
  
  <script>
  import GrandChildComponent from './GrandChildComponent.vue';
  
  export default {
    components: {
      GrandChildComponent
    },
    methods: {
      forwardData(data) {
        this.$emit('send-data', data);
      }
    }
  };
  </script>
  
  <style scoped>
  .child {
    background: #fafafa;
    border-radius: 8px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    padding: 15px;
    margin-bottom: 20px;
  }
  
  h2 {
    font-size: 22px;
    color: #444;
  }
  </style>
  