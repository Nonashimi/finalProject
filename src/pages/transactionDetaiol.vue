<template>
<div class="data">
        <formBreadVrumb :items = "arr" :label = "label" color ="#428777" ></formBreadVrumb>
</div>
<div class="sections">
    <div class="section1">
        <div class="head_flex">
            <div class="formTexts">
            <formText label = "#0123456" size = "24px"></formText>
            <formText label = "March 07,2021" size ="13px"></formText>
        </div>
        <div class="buttons_head">
            <buttonFr textColor="#c6cfde" label = "Print" color="#fff"  padding="10px 20px" border= "1px solid #c6cfde" ><i class="fa-solid fa-print"></i></buttonFr>
            <buttonFr textColor="#fff" label = "Download" color="#428777"  padding="10px 20px"  ><i class="fa-solid fa-download"></i></buttonFr>
</div>
        </div>

            <div class="info">
                <div class="infoPart">
                    <div class="title">Client</div>
    <div class="name">Samantha W.</div>
                </div>
                <div class="infoPart">
                    <div class="title">Company</div>
    <div class="name">ABC Studio</div>
                </div>
                <div class="infoPart">
                    <div class="title">Payment Type</div>
    <div class="name">Paypal</div>
                </div>

        </div>
       <div class="total">
        <FormText label = "Service" size = '15px' fontWeight="600"></FormText>
        
        <div class="oko">
            <FormText label = "Web Design + Development" size = '14px'></FormText>
      <FormText label = "$750.00"></FormText>
        </div>
        <div class="oko">
            <FormText label = "Hosting" size = '14px'></FormText>
      <FormText label = "$50.00"></FormText>
        </div>
        <formDivider margin = "30px 0"></formDivider>
        <div class="oko">
            <FormText label = "Subtotal" size = '14px'></FormText>
      <FormText label = "$800.00"></FormText>
        </div>
        <div class="oko">
            <FormText label = "Tax" size = '14px'></FormText>
      <FormText label = "$10.00"></FormText>
        </div>
        <div class="oko">
            <FormText label = "Total" size = '14px' fontWeight = "600"></FormText>
      <FormText label = "$810.00"  fontWeight = "600"></FormText>
        </div>
        
       </div>
       <FormCards title = 'Node:'></FormCards>
    </div>
    <div class="section2">
        <creditCard  cardNumber="Balance" cardBalance = "$4811,21"
      cardHolderName="John Doe"
      expiryDate="12/23"
      cardNumb = "1234567890121234">
    </creditCard>
    </div>
</div>
</template>

<script>
import formBreadVrumb from '@/components/formBreadVrumb.vue';
import formText from '@/components/formText.vue';
import buttonFr from "@/components/button_button.vue";
import creditCard from '@/components/creditCard.vue';
import FormText from '@/components/formText.vue';
import formDivider from '@/components/formDivider.vue';
import FormCards from '@/components/FormCards.vue';
export default{
    components:{
    formBreadVrumb,
    formText,
    buttonFr,
    creditCard,
    FormText,
    formDivider,
    FormCards
}
    ,data(){
        return{
            arr:["Transaction"],
            label :"#123456",

        }
    }
}

</script>

<style scoped>
.data{
    margin-left: 50px;
}
i{
    margin-right: 10px;
}
.buttons_head{
    display: flex;
    gap: 20px;
    margin-left: auto;
}
.head_flex{
    display: flex;
}

.oko{
 display: flex;
 justify-content: space-between;
 padding: 15px 0;
}
.total{
    padding: 20px;
    background-color: #efefef;
    border-radius: 13px;
}
.title{
    font-size: 15px;
    padding-bottom: 10px;
}
.info{
    padding: 40px 0 20px;
    display: flex;
    gap: 70px;
}
.name{
    font-size: 20px;
    font-weight: 600;
}
.sections{
    width:1200px;
    display: flex;
    gap: 5%;
}
.section1{
    width:65%;
    margin-left: 5%;
    margin-top: 25px;
}
.section2{
    width:30%;
}
</style>