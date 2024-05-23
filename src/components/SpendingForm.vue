<template>
<div class="spend" :style ="{backgroundColor:color}">
    <div class="title">{{ title }}</div>
    <div class="prob">{{ prob }}</div>

    <ChartsCircleVue :data ="value"  color = "#fff" class = "ddd"></ChartsCircleVue>
</div>
</template>

<script>
import ChartsCircleVue from './ChartsCircle.vue';
export default{
    props:{
        title:String,
        prob:String,
        color:String,
    value:Number,
    },
    components:{
        ChartsCircleVue
    },
   



}

</script>

<style scoped>
.spend{
    padding: 10px 15px;
    background-color: #428777;
    color: #fff;
    border-radius: 13px;
    width: 210px;
    font-size: 13px;
}
.ddd{
    float: right;
}
.title{
    padding-bottom: 10px;
}
</style>