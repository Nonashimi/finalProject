<template>
<div class="card" :style="{backgroundColor: color ,width: windth , height: height}">
<div class="circle1"></div>
<div class="circle2"></div>
<div class="circle3"></div>
</div>
</template>

<script>
export default{
props:{
    color:{
        type:String,
        default:"#428777"
    },
    width:{
        type:String,
        default:"50px"
    },
    height:{
        type:String,
        default:"30px"
    }
}
}

</script>

<style scoped>
.card{
    border-radius: 4px;
    position: relative;

}
.circle1{
    width: 30px;
    height: 30px;
    border-radius: 50%;
    border: 1px solid #fff;
    position: absolute;
    top: 40%;
    left:60% ;
}
.circle2{
    width: 20px;
    height: 20px;
    border-radius: 50%;
    border: 1px solid #fff;
    position: absolute;
    top: 60%;
    left:73% ;
}
.circle3{
    width: 10px;
    height: 10px;
    border-radius: 50%;
    border: 1px solid #fff;
    position: absolute;
    top: 75%;
    left:83% ;
}

</style>