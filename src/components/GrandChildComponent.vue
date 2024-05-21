<template>
    <div class="grandchild">
      <button @click="sendData('fikri, rian, adit')">Kelompok 1</button>
      <button @click="sendData('ali, andre, aji')">Kelompok 2</button>
      <button @click="sendData('mail, fizi, ipin')">Kelompok 3</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData(data) {
        this.$emit('send-data', data);
      }
    }
  };
  </script>
  
  <style scoped>
  .grandchild {
    background: #f0f0f0;
    border-radius: 8px;
    padding: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  
  button {
    background: #007BFF;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    margin: 5px 0;
  }
  
  button:hover {
    background: #0056b3;
  }
  </style>
  