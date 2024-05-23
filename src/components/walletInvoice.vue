<template>
<div class="flex" :style = "{width: width , backgroundColor: color}">
<div class="icon" >
    <formIcons :iconType = "type" size="25px" :color ="color"></formIcons>
</div>
<div class="text">{{ text }}</div>
</div>

</template>

<script>
import formIcons from './formIcons.vue';
export default{
    components:{
        formIcons,
    }
    ,
    props:{
    text:String,
    width:String,
    color:String,
    type:String,
    }
}


</script>

<style scoped>
.icon{
    width:30px;
    padding: 7px;
    border-radius: 4px;
    background-color:#fff;
}
.flex{
    display: flex;
    gap: 40px;
    align-items: center;
    font-size: 19px;
    padding: 15px 20px;
    border-radius: 13px;
    background-color: #ee4444;
    color: #fff;
    justify-content: center;
}
.text{
    width: 120px;
}



</style>