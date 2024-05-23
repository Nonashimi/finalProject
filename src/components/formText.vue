<template>
<div class="text" :style="{color: color , fontWeight: fontWeight , fontSize: size,padding: padding}">{{ label }}</div>
</template>

<script>
export default{
    props:{
        color:{
            type:String,
            default:"black",
        },
        fontWeight:{
            type:String,
            default:"500",
        },
        size:{
            type:String,
            default:"16px"
        },
        padding:{
            type:String,
            default:""
        },
        label:String
    }
}

</script>

<style scoped>
.text{
    letter-spacing: 1.2;
}
</style>