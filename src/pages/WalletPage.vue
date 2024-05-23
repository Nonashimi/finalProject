<template>
<div class="wallet_contain">
    <div class="part1">
    <div class="flex">
        <balanceCredit  cardNumber="Balance" cardBalance = "$4811,21"
      cardHolderName="John Doe"
      expiryDate="12/23"
      cardNumb = "1234567890121234" width = "55%">
    </balanceCredit>       
   <walletInvoiceGroup width = "35%"></walletInvoiceGroup>
    </div>
    <div class = "lastInv">
        <walletSectionInv></walletSectionInv>
    </div>
       
</div>
    <div class="part2">
        <invoicesSent></invoicesSent>
    </div>

</div>
</template>

<script>
import walletInvoiceGroup from "@/components/walletInvoiceGroup.vue";
import balanceCredit from '@/components/balanceCredit.vue';
import walletSectionInv from "@/components/walletSectionInv.vue";
import invoicesSent from "@/components/InvoicesSent.vue";
export default{
    components:{
        balanceCredit,
        walletInvoiceGroup,
        walletSectionInv,
        invoicesSent
    }
}

</script>

<style scoped>
.wallet_contain{
    display: flex;
    width:1200px;
    gap: 5%;
    margin:0 40px;
}
.flex{
    display:flex;
    gap:5%;
    margin-left: 20px;
}
.part1{
    width: 70%;
    
}
.part2{
    width: 23%;
 

}
.lastInv{
    width:92%;
    margin: 0 auto
}


</style>