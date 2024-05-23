<template>
<div class="flex" :style ="{color: color}" @click="clickDrop">
    <div class="title">{{ label }}</div>
    <div class="upDown"><i class="fa-solid fa-chevron-up"></i></div>
</div>
</template>

<script>
export default{
 props:{
    label:String,
    color:String,

 },
 data(){
    return{
        isClick:false,
    }
 },
 methods:{
    clickDrop(){
        let upDown = document.querySelector(".upDown");
        if(this.isClick){
        upDown.classList.add("isTran");
        this.isClick = !this.isClick

        }else{
            upDown.classList.remove("isTran");
            this.isClick = !this.isClick

        }
    }
 }
}

</script>

<style scoped>
.upDown{
    margin-left: 10px;
    transition: all .2s;
}
.title{
    cursor: pointer;
}
.isTran{
    transform: rotate(3.142rad);
}
</style>