<template>
<div class="">
    
<button :style = "{backgroundColor: color , padding: padding, border: border ,color:`${textColor}`}"><slot></slot>{{ label }}</button>

</div>
</template>

<script>
export default{
    props:{
        label:String,
        color:String,
        padding:String,
        textColor:String,
        border:{
            type:String,
            default:"none"
        }
    },
    data(){
        
    }
}


</script>

<style scoped>
button{
    color: #fff;
    font-weight: 400;
    border-radius: 3px;
    cursor: pointer;
}
</style>