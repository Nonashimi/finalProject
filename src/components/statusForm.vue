<template>
<div class="stat" :style ="{border: `1px solid ${color}` , color : color}">
{{ label }}
</div>
</template>

<script>
export default{
    props:{
        color:String,
        label:String,
    }
}

</script>

<style scoped>
.stat{
    background-color: #fff;
    padding: 4px 6px;
    border-radius: 3px;
}

</style>