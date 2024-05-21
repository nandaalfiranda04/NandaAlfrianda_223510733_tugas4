<template>
    <div class="parent">
      <h1>Daftar Nama Kelompok 4A PBK</h1>
      <p>Data Kelompok : {{ receivedData }}</p>
      <ChildComponent @send-data="handleData">
      </ChildComponent>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent
    },
    data() {
      return {
        receivedData: ''
      };
    },
    methods: {
      handleData(data) {
        this.receivedData = data;
      }
    }
  };
  </script>
  
  <style scoped>
  .parent {
    background: #ffffff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    margin-bottom: 20px;
  }
  
  h1 {
    font-size: 24px;
    color: #333;
  }
  
  p {
    font-size: 18px;
    color: #666;
  }
  
  .slot-content {
    background: #e0e0e0;
    padding: 10px;
    border-radius: 4px;
    margin-top: 10px;
    font-size: 16px;
  }
  </style>
  