<template>
    <div class="grid-container">
      <div class="grid_row">
        <creditCard  cardNumber="Balance" cardBalance = "$4811,21"
         cardHolderName="John Doe"
         expiryDate="12/23"
         cardNumb = "1234567890121234">
        </creditCard>
  <chartForm :datasets = "[{
      label: 'Income',
      backgroundColor: '#428777',
      borderColor: '#428777',
      data: [0, 20, 30, 25, 50,40,50 ,100,56,60],
      tension:.5,
    }] " id = "income"></chartForm>
     <chartForm :datasets = "[{
      label: 'Outcome',
      backgroundColor: '#ee4444',
      borderColor: '#ee4444',
      data: [60, 56, 30, 50, 40,50,25 ,30,20,0],
      tension:.5,
    }] " id = "outcome"></chartForm>
    
<ChartsCircleVue data ="75" limit ="Limit"></ChartsCircleVue>
      </div>
     <div class="grid_row">
      <ChartsBar></ChartsBar>
      <SpendGroups></SpendGroups>
     </div>
     <div class="grid_row">
      <div class="">
<spendTitle name = "Lastest Invoices"></spendTitle>
<LastinvoiceGroup width = '500px'></LastinvoiceGroup>

      </div>
   <tranSactionGroup></tranSactionGroup>
     </div>


    </div>
  </template>
  
  <script>
  import creditCard from './creditCard.vue';
  import ChartsCircleVue from './ChartsCircle.vue';
  import SpendGroups from "./Spend_Groups.vue";
  import tranSactionGroup from './tranSactionGroup.vue';
  import LastinvoiceGroup from './LastinvoiceGroup.vue';
  import spendTitle from './spendTitle.vue';
  import ChartsBar from './ChartsBar.vue';
  import chartForm from "./chartsForm.vue";

  // import ChartsBar from './ChartsBar.vue';
  // import Spending from "./SpendingForm.vue";
  export default {
    data() {
      return{
      }
     
    
    },
    components:{
      chartForm,
      creditCard,
      ChartsCircleVue,
      SpendGroups,
      tranSactionGroup,
      LastinvoiceGroup,
      spendTitle,
      ChartsBar
      // ChartsBar,
      // Spending
    }
  };
  </script>
  
  <style scoped>

  .grid_row{
    display: flex;
    gap: 60px;
    margin-bottom: 40px;
    margin-left: 40px;
  }
  
 
  .grid-item {
    background-color: #f0f0f0;
    
    text-align: center;
  }

 
  </style>
  