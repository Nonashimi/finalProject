<template>
<div class="flex" :style="{width: width}">
    <div class="invoice">
        <formCheckbox></formCheckbox>
<div class="id">{{ id }}</div>
    </div>
<div class="rec">{{ recipient }}</div>
<div class="date">{{ date }}</div>
<statusForm :color = "color" :label = "label" ></statusForm>
</div>
</template>

<script>
import formCheckbox from './formCheckbox.vue';
import statusForm from './statusForm.vue';
export default{
    props:{
      id:String,
      recipient:String,
      date:String,
      color:String,
      label:String,
      width:String,

      
    },
    components:{
    formCheckbox,
    statusForm,
}
}
</script>


<style scoped>
.flex{
 
    gap: 15%;
    padding: 11px 0;
}
.invoice{
    display: flex;
    gap:10px;
}
.id{
   width:100px;
}
.rec{
    width:100px;
}
.date{
    width:150px;
  
}

</style>