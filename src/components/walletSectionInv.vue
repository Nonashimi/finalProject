<template>
    <div class="pad">
        <div class="spend_title">
          <div class="spend_name">Lastest Invoices</div>
          <div class="spend_icon">
            <groupButton></groupButton>
          </div>
        </div>
<LastinvoiceGroupVue width = "100%"></LastinvoiceGroupVue>

    </div>
</template>


<script>
import groupButton from "./groupButton.vue";
import LastinvoiceGroupVue from "./LastinvoiceGroup.vue";
export default{
    components:{
        groupButton,
        LastinvoiceGroupVue
    }
}

</script>


<style scoped>

.spend_title{
    display: flex;
    margin-bottom:30px;
  }
  .pad{
    padding: 40px 0;
  }
  .spend_icon{
    margin-left: 50%;
    font-size: 20px;
    border-radius: 30px;
    color: #9babc5;
    background-color:rgb(201, 199, 199);
  }
  .spend_name{
    font-size: 21px;
  }
</style>