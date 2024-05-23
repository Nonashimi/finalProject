<template>
    <div class="all" @click="clickOn">
        <div class="bd" ><div class="" v-html="label"></div><div class="badge"></div></div>
      
    </div>
</template>


<script>
export default{
    props:{
        value:{
            value:String,
            default:"0"
        }
        ,label:String,

    }
    ,
    data(){
        return{
            data:"",
        }
      
    },
    methods:{
        clickOn(){
        }
    }
}

</script>

<style scoped>
.all{
    font-size: 20px;
    font-family: 'Roboto', sans-serif;
    position: relative;
   
}
.bd{
    position: relative;
 width:20px;
 color: gray;
}
.badge{
    font-size: 16px;
    position: absolute;
    background-color: #198568;
    color: #fff;
    width: 8px;
    height: 8px;
    border-radius: 50px;
    top: -4px;
    right:-12px;
}

</style>