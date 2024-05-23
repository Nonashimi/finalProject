<template>

<div class="spend">
        
        <div class="spend_title">
          <div class="spend_name">Spending</div>
          <div class="spend_icon"><i class="fa-solid fa-ellipsis"></i></div>
        </div>
        <div class="grid_sqare">
        <Spending  value = "25" title = "Subcription" prob = "$500 / $2000" color ="#428777"></Spending>
      <Spending  value = "50" title = "Groceries" prob = "$1000 / $2000" color ="#f0ca43"></Spending>
      <Spending  value = "10" title = "Invesment" prob = "$50 / $2000" color ="#9babc5"></Spending>
      <Spending  value = "75" title = "Others" prob = "$1500 / $2000" color ="#ee4444"></Spending>

    </div>
      </div>
</template>

<script>
import Spending from "./SpendingForm.vue";
export default{
   components:{
    Spending
   }
}
</script>

<style scoped>
 .spend_title{
    display: flex;
    margin-bottom: 10px;
    
  }
  .spend_icon{
    float: right;
    margin-left: 390px;
    font-size: 20px;
    color: #9babc5;
  }
  .spend_name{
    font-size: 21px;
  }
  .spend{
    float: right;
  }
  .grid_sqare{
    display:flex;
    width: 500px;
    flex-wrap: wrap;
    gap: 20px;
   
  }

</style>