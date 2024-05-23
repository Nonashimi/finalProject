<template>
<div class="card">
<div class="title">{{ title }}</div>
<div class="subtitle">{{ subtitle }}</div>
<div class="text">{{ text }}</div>
</div>
</template>

<script>
export default{
    props:{
        title:String,
        subtitle:String,
        text:{
            text:String,
            default:"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Repudiandae dolor magni libero quas! Praesentium voluptate quisquam consequuntur recusandae tempora accusamus nemo mollitia illum eius, excepturi laudantium aspernatur,doloribus facere id.",
        }
    },
    data(){

    },
    methods:{

    }
}
</script>

<style scoped>
.card{
    margin-top: 30px;
    margin-bottom: 50px;
    padding:  20px;
    font-size: 20px;
    background-color: #efefef;
    font-family: 'Roboto', sans-serif;
    border-radius: 13px;
}
.title{
    font-size: 17px;
    font-weight: 600;
    margin-bottom: 20px;
}
.subtitle{
    color: rgb(180, 176, 176);
    margin-bottom: 4px;
}
.text{
    font-size: 16px;
    color: rgb(75, 73, 73);
}
</style>