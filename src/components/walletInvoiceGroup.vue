<template>
    <div class="block">
        <walletInvoice text= "Transfer" width="100%" color = "#428777" class = "wallIn wall" type="transfer"></walletInvoice>
    <walletInvoice text= "Send Invoice" width="100%" color = "#f0ca43"  type = "send"></walletInvoice>

    </div>
   
</template>

<script>
import walletInvoice from '@/components/walletInvoice.vue'
export default{
    components:{
        walletInvoice
    },
    props:{
        type:String,
    }
   
}

</script>

<style scoped>
.wallIn{
    margin-bottom: 30px;
}

</style>