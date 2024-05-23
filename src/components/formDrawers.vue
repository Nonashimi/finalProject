<template>
    <div>
      <div v-show="isDrawerOpen" class="drawer">
        <div class="icon"  >
        <formIconsVue size = "35px" color  ="#428777" iconType ="bank"></formIconsVue>
      <div class="iconName">Bilpay</div>
    </div>
    <formListGroupVue @sendData="send"></formListGroupVue>
      </div>
      <div ><slot></slot></div>
  
     
    </div>
  </template>
  
  <script>
  import formIconsVue from './formIcons.vue';
  import formListGroupVue from './formListGroup.vue';
  export default {
   
    data() {
      return {
        isDrawerOpen: true,
      };
    },
    methods: {
      send(data){
        if(data == "Card"){
          data = "Cards Center";
        }else if(data == "Invoices"){
          data = "Invoice Detail";
        }else if(data == "Transaction"){
          data = "Transaction Detail";
        }
        this.$emit('sendData', data);
      }
      ,
      toggleDrawer() {
        this.isDrawerOpen = !this.isDrawerOpen;
      },
      closeDrawer() {
        this.isDrawerOpen = false;
      },
    },
    components:{
      formIconsVue,
      formListGroupVue
    }
  };
  </script>
  
  <style scoped>
  .drawer {
    position: fixed;
    top: 0;
   left:0;
   width: 258px;
    height: 100%;
    background-color: #ffffff;
    box-shadow: -2px 0 5px rgba(0, 0, 0, 0.1);
    z-index: 999;
    overflow-y: auto;
  }
  .icon{
    padding: 20px 0;
    display: flex;
    cursor: pointer;
    width: 240px;
    margin: 3px 0;
    text-align: center;
   
    justify-content: center;
   gap: 10px;
}


.iconName{
  align-items: center;
    color: #111111;
    font-size: 25px;
    font-weight: 800;
    margin-top: 3.3%;
}
  </style>
  