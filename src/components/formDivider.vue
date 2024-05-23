<template>
    <div class="divider" :style="{ backgroundColor: `${bacColor}` , margin: margin }"></div>
  </template>
  <script>
 export default{
    props:{
        bacColor:{
            type:String,
            default:"#ccc"
        },
        margin:{
          type:String,
          default:"",
        }
    }
 }

</script>

  <style scoped>
  .divider {
    height: 1px;
    width: 100%;
  }
  </style>