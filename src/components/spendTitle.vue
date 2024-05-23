<template>
<div class="spend_title">
          <div class="spend_name">{{ name }}</div>
          <div class="spend_icon"><i class="fa-solid fa-ellipsis"></i></div>
        </div>


</template>

<script>
export default{
    props:{
        name:String,
    }
}


</script>

<style scoped>


.spend_title{
    display: flex;
    margin-bottom: 10px;
    justify-content: space-between;
  }
  .spend_icon{
    float: right;
    
    font-size: 20px;
    color: #9babc5;
  }
  .spend_name{
    font-size: 21px;
  }
</style>