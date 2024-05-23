<template>
    <div class="search-bar">
      <i class="fa-solid fa-magnifying-glass"></i>
      <input
        :type="type"
        v-model="searchQuery"
        :placeholder="placeholder"
        @input="handleInputChange"
      />
    </div>
  </template>
  
  <script>
  export default {
    props:{
     placeholder:String,
     type:{
      type:String,
      default:"text"
     }
    },
    data() {
      return {
        searchQuery: "",
      };
    },
    methods: {
      handleInputChange() {
        console.log("Изменение ввода:", this.searchQuery);
      },
   
    },
  };
  </script>
  
  <style scoped>
  .search-bar {
    display: flex;
    width:60% ;
    position: relative;
  }
  i{
    color: #428777;
    position: absolute;
    font-size: 20px;
    bottom: 20%;
    left: 0.5%;
  }
  
  input {
    padding: 7px 0 7px 35px;
    font-size: 16px;
    color: rgb(169, 167, 167);
    width:100%;
    outline: none;
    border: none;
  }
  
  button {
    padding: 8px 12px;
    font-size: 16px;
    cursor: pointer;
  }
  </style>
  