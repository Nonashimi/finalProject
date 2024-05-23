    <template>
    <div class="">
        <div class="Credits">
        <creditCard  cardNumber="Balance" cardBalance = "$4811,21" cardHolderName="John Doe" expiryDate="12/23" cardNumb = "1234567890121234"></creditCard>
        <mediumCreditCard  cardNumber="Balance" cardBalance = "$4811,21" cardHolderName="John Doe" expiryDate="12/23" cardNumb = "1234567890121234" width="211px" height="150px" color="#f0ca43"></mediumCreditCard>
        <mediumCreditCard  cardNumber="Balance" cardBalance = "$4811,21" cardHolderName="John Doe" expiryDate="12/23" cardNumb = "1234567890121234" width="211px" height="150px" color="#ee4444"></mediumCreditCard>
        <mediumCreditCard  cardNumber="Balance" cardBalance = "$4811,21" cardHolderName="John Doe" expiryDate="12/23" cardNumb = "1234567890121234" width="211px" height="150px" color="#9babc5"></mediumCreditCard>
        </div>

        <div class="sections">
        <div class="section1">
            <FormText label = "Card List" fontWeight = "600" size ="20px"></FormText>
            <formTables></formTables>
        </div>
        <div class="section2">
            <div class="AddingCard">
                <FormText label = "Add Card" fontWeight = "600" size ="20px"></FormText>
        <div class="inputs">
            <div class="input">
            <FormText label = "Card Number" size="17px"></FormText>
            <TextInput placeholder="Card Number..."></TextInput>
        </div>
        <div class="input">
            <FormText label = "Bank" size="17px"></FormText>
            <TextInput placeholder="Bank"></TextInput>
        </div>
        <div class="input">
            <FormText label = "Namein Card" size="17px"></FormText>
            <TextInput placeholder="Name..."></TextInput>
        </div>
        </div>
        <div class="buttons">
            <Btn label = "Add Card" color = "#428777" padding ="10px 32.5%"><i class="fa-regular fa-square-plus"></i></Btn>
        </div>   
        </div>
        </div>
        </div>
    </div>
    </template>

<script>
import creditCard from '@/components/creditCard.vue';
import FormText from '@/components/formText.vue';
import formTables from '@/components/FormTables.vue';
import mediumCreditCard from '@/components/mediumCreditCard.vue';
import TextInput from '@/components/TextInput.vue';
import Btn from "@/components/button_button.vue";
export default{
    components:{
    creditCard,
    mediumCreditCard,
    FormText,
    TextInput,
    formTables,
    Btn
}
}
</script>

<style scoped>
.Credits{
    display: flex;
    gap: 40px;
    align-items: center;
    margin-left: 60px;
    margin-top: 40px;
}

.sections{
    width:1200px;
    display: flex;
    gap: 5%;
    margin-bottom: 100px;
}
i{
    margin-right: 20px;
}
.inputs{
    margin-top: 25px;
}
.section1{
    width:75%;
    margin-left: 7%;
    margin-top: 70px;
}
.input{
    margin-bottom: 15px;
    display: grid;
    gap: 15px;
}
.buttons{
    margin-top: 50px;
}
.section2{
    width:25%;
    margin-top: 70px;
}
</style>