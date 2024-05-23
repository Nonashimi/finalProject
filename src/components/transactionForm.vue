<template>
    <div class="flex">
        <div class="fon_flex">
            <div class="fon" :style="{backgroundColor: color}">
            <formIcons :iconType="type" color ='#fff' size = "30px"></formIcons>

        </div>
    <div class="tran_title">{{ title }}</div>
        </div>
      
    <div class="tran_date">{{ date }}</div>
    <div class="tran_money">{{ money }}</div>
    <button_button :label = "label" padding ="5px 7px" :color = "color"></button_button>
    </div>
</template>

<script>
import formIcons from './formIcons.vue';
import button_button from './button_button.vue';
export default{
    props:{
     title:String,
     date:String,
     money:String,
     color:String,
     type:String,
     label:String
    },
    components:{
    formIcons,
    button_button,
   
}
}
</script>

<style scoped>
.fon{
    padding: 4px 8px;
    border-radius: 3px;
}
.flex{
    width: 500px;
    display: flex;
    font-size: 12px;
    align-items: center;
    padding: 20px 0;
}
.tran_title{
    font-weight: 600;
    width: 115px;
}
.fon_flex{
    display: flex;
    gap: 20px;
    align-items: center;
    margin-right: 60px;
}
.tran_date{
    color: #c5cfdd;
    font-size: 10px;
    margin-right: 30px;
}
.tran_money{
    font-size: 15px;
    margin-right: auto;
}

</style>