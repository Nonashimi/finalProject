<template>
<div class="profile">
    <formProfileImageVue :src = "src"></formProfileImageVue>
   <div class="title">
    <div class="name">{{ name }}</div>
    <div class="ago">{{ ago }}</div>
   </div>
   <div class="prib">
    {{ prib }}
   </div>
</div>
</template>

<script>
import formProfileImageVue from './formProfileImage.vue';
export default{
    components:{
    formProfileImageVue
},
props:{
    name:String,
    ago: String,
    prib:String,
    src:String,
}
}

</script>

<style scoped>

.name{
    font-size: 15px;
    font-weight: 600;
    width:120px;
    
  }
  .prib{
    color: #428777;
    font-weight: 600;
  }
  .ago{
    font-size: 12px;
    color: #9babc5;
    margin-top: 2px;
  }
  .profile{
    display: flex;
    align-items: center;
    padding: 10px 0;
  }
  .title{
    margin-left: 20px;
    margin-right: 17%;
  }

</style>