<template>
    <nav class="breadcrumb">
      <ul :style="{ backgroundColor: `${bacColor}` }">
        <li v-for="(item, index) in items" :key="index" :style = "{color: color}">
            <div class="category">{{ item }} <span class="slsh">  /</span></div>
        </li>
        {{ label }}
      </ul>
    </nav>
  </template>

  <script>
  export default {
    props: {
      items: {
        type: Array,
        default: () => [],
      },
      bacColor:{
        type:String,
        default:"#fff"
      },
      color:String,
      label:String,
    },
  };
  </script>
  
  <style scoped>
  .breadcrumb {
    margin-bottom: 20px;
  }
  
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
    color: rgb(168, 160, 160);
  }
  
  li {
    display: inline-block;
    margin-right: 5px;
  }
  .slsh{
    font-size: 20px;
  }
  .category{
    font-size: 20px;
    font-family: 'Roboto', sans-serif;

  }
  .breadcrumb ul{
    padding: 10px 10px;
    width:500px;
  }
  
  
  </style>
  