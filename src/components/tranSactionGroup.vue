<template>

<div class="transaction_gr">
  <div class="spend_title">
          <div class="spend_name">Previous Transaction</div>
          <div class="spend_icon"><i class="fa-solid fa-ellipsis"></i></div>
        </div>
<DropDownButton label = 'Bulan Ini' color ="#9babc5"></DropDownButton>
  <transaction title = "Netflix Subcription" date  = "March 2,2021" money ="+$45" color = "#428777" type = 'up' label="Completed"></transaction>
  <formDivider></formDivider>
  <transaction title = "PayPal Payment" date  = "March 2,2021" money ="+$480" color = "#ee4444" type = "down" label ="Canceled"></transaction>
  <formDivider></formDivider>
  <transaction title = "Spotify Subciption" date  = "March 2,2021" money ="+$16" color = "#f0ca43" type = "up" label ="Pending"></transaction>
  <formDivider></formDivider>

</div>

</template>


<script>
import transaction from './transactionForm.vue';
import formDivider from './formDivider.vue';
import DropDownButton from './DropDownButton.vue';
export default{
    components:{
        transaction,
        formDivider,
        DropDownButton
    }
}
</script>


<style scoped>

.spend_title{
    display: flex;
    margin-bottom:30px;
    
  }
  .spend_icon{
    float: right;
    margin-left: 275px;
    font-size: 20px;
    color: #9babc5;
  }
  .spend_name{
    font-size: 21px;
  }
</style>