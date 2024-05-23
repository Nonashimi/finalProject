<template>
    <div class="block">
        <div class="flex fff" :style = "{width: width}">
    <div class="invoice">
        <formCheckbox></formCheckbox>
<div class="id">ID Invoices</div>
    </div>
<div class="rec">Recipient</div>
<div class="date">Date</div>
<div class="status">Status</div>
</div>
<formDivider></formDivider>
<LastInvoice id = "INV-001-123" recipient = "Rob B." date = "March 10, 2021" color="#428777" label = "Paid" :width = "width"></LastInvoice>
<LastInvoice id = "INV-002-123" recipient = "Karen A." date = "March 9, 2021" color="#ee4444" label = "Unpaid" :width = "width"></LastInvoice>
<LastInvoice id = "INV-003-123" recipient = "Karen H." date = "March 8, 2021" color="#ee4444" label = "Unpaid" :width = "width"></LastInvoice>
<LastInvoice id = "INV-004-123" recipient = "Johnny A." date = "March 7, 2021" color="#428777" label = "Paid" :width = "width"></LastInvoice>
<LastInvoice id = "INV-005-123" recipient = "Rob B." date = "March 6, 2021" color="#428777" label = "Paid" :width = "width"></LastInvoice>

    
    </div>
     
</template>

<script>
import LastInvoice from './LastInvoice.vue';
import formDivider from './formDivider.vue';
import formCheckbox from './formCheckbox.vue';
export default{
  components:{
    LastInvoice,
    formDivider,
    formCheckbox
  },
  props:{
    width:String,
  }
}
</script>

<style scoped>


  .flex{
    gap: 7%;
}
.fff{
    padding: 20px 0;
}

.invoice{
    display: flex;
    gap:5%;
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