<template>
<div class="flex">
<div class="data">
    <div class="title">{{ title }}</div>
    <div class="text">{{ text }}</div>
</div>
<formProfileImage src= "https://thicc-af.mywaifulist.moe/waifus/yuta-okkotsu-sorcery-fight/3DQkg87cFXIigaUzRunm7v3bLXIWTc9BLePplwFu.jpg?class=thumbnail"></formProfileImage>


</div>
</template>

<script>
import formProfileImage from './formProfileImage.vue';
export default{
  components:{
    formProfileImage
  }
  ,
  props:{
    title:String,
    text:String
  },
  methods:{

  }
}

</script>

<style scoped>
.flex{
    display: flex;
    gap:20px;
    align-items: center;
}
.title{
    font-size: 13px;
}
.text{
    font-size: 13px;
    color: gray;
}

</style>