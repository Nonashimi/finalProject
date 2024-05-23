  <template>
    <formDrawers @sendData = "drop"></formDrawers>
    <formPageHeader></formPageHeader>
    <div class="flex">
      <div class="space"></div>
  <div class="block">
  <formText :label ="parts" color="black" size = "25px" fontWeight = "600" class ="dd" ></formText>
  <formGridSystem v-if = "parts==`Dashboard`"></formGridSystem>
  <WalletPage v-if = "parts==`Wallet`"></WalletPage>
  <transactionDetaiol v-if = "parts =='Transaction Detail'"></transactionDetaiol>
  <invoicesDetail v-if = "parts =='Invoice Detail'"></invoicesDetail>
  <CardCenterPage v-if = "parts ==`Cards Center`"></CardCenterPage>
  </div>
    </div>
    
  </template>

<script>
import formPageHeader from './components/formPageHeader.vue';
import formDrawers from './components/formDrawers.vue';
import formText from './components/formText.vue';
import transactionDetaiol from './pages/transactionDetaiol.vue';
import invoicesDetail from './pages/invoicesDetail.vue';
import CardCenterPage from "./pages/CardCenterPage.vue";
import formGridSystem from './components/formGridSystem.vue';
import WalletPage from "./pages/WalletPage.vue";
export default {
  name: 'App',
  components: {
    formPageHeader,
    formDrawers,
    formText,
    WalletPage,
    CardCenterPage,
    transactionDetaiol,
    invoicesDetail,
    formGridSystem
  },
  data(){
    return{
      parts:"Dashboard",
    }
    
  },
  methods:{
    drop(data){
       this.parts = data;
    }
  }
}
</script>

<style >
*{
  font-family: 'Open Sans', sans-serif;}
  body{
    margin: 0;
  }
  .space{
   width:258px;
   height: 100vh;
   background-color:rgb(61, 53, 53);
  }
  .flex{
    display: flex;
  }
  .spend_title{
    display: flex;
    margin-bottom: 10px;
    
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
  
  .dd{
    margin: 10px 0 10px 60px;
  }
</style>
