<template>
    <div class="data">
        <formBreadVrumb :items = "arr" :label = "label" color ="#428777" >
        </formBreadVrumb>
    </div>
    <div class="sections">
        <div class="section1">
            <div class="head_flex">
                <div class="formTexts">
            <formText label = "Invoice" size = "13px"></formText>
            <formText label = "#0123456" size ="24px"></formText>
        </div>
        <div class="buttons_head">
            <buttonFr textColor="#428777" label = "Paid" color="#ecf3f1"  padding="10px 20px" ><i class="fa-solid fa-circle-check"></i></buttonFr>
        </div>
            </div>
            <div class="info">
    <div class="oko">
        <div class="icons">
            <formProfileImage src ="https://pics.craiyon.com/2023-05-30/eaab7f873e324b3e8f41f5aba2c2aeb2.webp"></formProfileImage>
         <div class="title">
           <formText label = "Client" color="#9eaec7"></formText>
           <formText  label = "Samantha W." padding="10px 0"></formText>
         </div>
        </div>
        <div class="titles">
            <formText label = "Due to" color="#9eaec7"></formText>
           <formText  label = "07 March, 2021"  padding="10px 0"></formText>
         </div>

    </div>
    <div class="oko">
        <div class="icons">
         <div class="title">
            <formText label = "Address" color="#9eaec7"></formText>
           <formText  label = "1234 Tamrin Street Awenue Jakarta 45678 Indonesia"  padding="10px 0"></formText>
           
         </div>
        </div>
        <div class="titles">
          <formText label = "Contact"></formText>
            <div class="name">
               +123 456 789 <br>
               email@mail.com
            </div>
         </div>

    </div>
    <div class="oko">
        <div class="icons">
         <div class="title">
            <formText label = "Bank Information" color = "#9eaec7" padding ="10px 0"></formText>
            <div class="name">
               National Bank <br> John Doe <br> 1234567
            </div>
         </div>
        </div>
    

    </div>


    <div class="formtexts">
<formText label = "Service" color="#9eaec7" size = "20px"></formText>
<formText label = "Amount" color="#9eaec7" size = "20px"></formText>

    </div>
<formDivider margin ="20px 0"></formDivider>
<div class="formtexts">
<formText label = "Web Design"  size = "20px"></formText>
<formText label = "$500"  size = "20px"></formText>

    </div>
    <div class="formtexts">
<formText label = "Web Development"  size = "20px" ></formText>
<formText label = "$1000"  size = "20px"></formText>

    </div>
    
    <div class="marTop">
        <div class="totalTexts">
    <formText label = "Subtotal"  size = "16px" ></formText>
    <formText label = "$1500.00"  size = "16px" ></formText>
</div>
<div class="totalTexts ">
    <formText label = "Discount (10%)"  size = "16px" ></formText>
    <formText label = "$150.00"  size = "16px" ></formText>

</div>
<div class="totalTexts ">
    <formText label = "Total"  size = "16px" fontWeight = "600" ></formText>
    <formText label = "$1350.00"  size = "16px" fontWeight = "600" ></formText>

</div>
    </div>


            </div>
        </div>
        <div class="section2">
            <div class="paymentUse">
                <formText label ="Payment Card Used" size ="20px" fontWeight = "600"></formText>
    <div class="miniCr">
        <miniCredit></miniCredit>
     <formText label ="Main Card" size ="14px"></formText>
     <formText label ="**** **** **** 1234" size = "14px"></formText>
    </div>
    <div class="insurance">
        <formText label ="Insurance Responsibility" size ="20px" fontWeight="600"></formText>
    </div>
    <div class="oap">
        <formText label ="Aetna - Open Access" size = "17px"></formText>
        <formText label = "OAP" size = "17px"></formText>
    </div>
            </div>
    

    <div class="grid">
        <div class="buttons_flex">
        <buttonFr textColor ="#fff" color ="#428777" label = "Mark as Paid" padding ="12px 30px"><i class="fa-regular fa-circle-check"></i></buttonFr>
        <buttonFr textColor ="#428777" color ="#fff" label = "Download" padding ="12px 30px"><i class="fa-solid fa-download"></i></buttonFr>

    </div>
    <div class="buttons_flex">
        <buttonFr textColor ="#428777" color ="#fff" label = "Print" padding ="12px 30px"><i class="fa-solid fa-print"></i></buttonFr>
        <buttonFr textColor ="#428777" color ="#fff" label = "Send" padding ="12px 30px"><i class="fa-regular fa-paper-plane"></i></buttonFr>

    </div>
    </div>
    
        </div>

        

    </div>

</template>

<script>
import formBreadVrumb from '@/components/formBreadVrumb.vue';
import formText from "@/components/formText.vue";
import buttonFr from "@/components/button_button.vue";
import formProfileImage from '@/components/formProfileImage.vue';
import formDivider from '@/components/formDivider.vue';
import miniCredit from '@/components/miniCredit.vue';
export default{
    components:{
     formBreadVrumb,
     formText,
     buttonFr,
     formProfileImage,
     formDivider,
     miniCredit
     
    },
    data(){
        return{
            arr:["Invoice"],
        label:'#123456'
        }
      
    }
}
</script>


<style scoped>
.data{
    margin-left: 50px;
}
.insurance{
    padding: 20px 0;
}
.grid{
    display: grid;
    gap: 20px;
    margin-top: 50px;
}
.buttons_flex{
    display: flex;
    justify-content: space-between;
}
.paymentUse{
    max-width: 90%;
    margin: 0 auto;
}
.oap{
    display: flex;
    justify-content: space-between;
    padding: 10px 0;
}
.miniCr{
    display: flex;
    gap:25px;
    align-items: center;
    padding: 30px 0;
}
.marTop{
    margin-top: 100px;
    width: 300px;
    float: right;
    margin-bottom: 100px;
}
i{
    margin-right: 10px;
    font-size: 17px;
}
.totalTexts{
    display: flex;
    width: 300px;
    padding: 10px;
    justify-content: space-between;

}

.formtexts{
    display: flex;
    justify-content: space-between;
    padding: 10px 0;
}
.oko{
    display: flex;
    padding: 35px 0;
}

.head_flex{
    display: flex;
}
.titles{
    margin-left: 20%;
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
.icons{
    display: flex;
    gap: 20px;
    width:300px;
}
.buttons_head{
    display: flex;
    gap: 20px;
    margin-left: auto;
}
.subtitle{
    color: #9eaec7;
    margin-bottom: 10px;
}
.section2{
    width:30%;
}
</style>