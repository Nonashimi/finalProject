<template>
    <div class="list-group">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="list-group-item"
        @click="selectItem(index)"
        :class="{ active: selectedIndex === index }"
      >
         <div class="ic" v-html="icons[index]"></div>   {{ item }}
         <div class="icon" v-html="ico[index]" :id ="`AS${index}`"></div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        items: ["Dashboard", "Wallet", "Invoices", "Create Invoices","Card","Transaction","Clients"],
        ico:["","","3","",`<i class="fa-solid fa-chevron-down"></i>`,"",""],
        selectedIndex:0,
        icons: [`<i class="fa-solid fa-table-columns"></i>`,`<i class="fa-solid fa-wallet"></i>`,`<i class="fa-solid fa-file-invoice-dollar"></i>`
        ,`<i class="fa-regular fa-square-plus"></i>`,`<i class="fa-regular fa-credit-card"></i>`,`<i class="fa-solid fa-arrows-spin"></i>`,`<i class="fa-solid fa-users"></i>`]
        ,
      }
    },
    methods: {
      selectItem(index) {
        this.selectedIndex = index;
        this.$emit('sendData', this.items[index]);

      },
    },
  };
  </script>
  
  <style scoped>
  .list-group {
    width: 75.5%;
    margin: 30px 0;
    
  }
  #AS2{
    padding: 2px 8px;
    background-color: red;
    color: #fff;
    margin-left: 25%;
    border-radius: 50%;
  }
  #AS4{
    margin-left: 37%;
  }
  
  .list-group-item {
    padding: 5px 0 5px 30%;
    margin: 10px 0 20px;
    width:100%;
    cursor: pointer;
    display: flex;
    color: gray;
    align-items: center;

    gap: 15px;
   
  }
  
  .list-group-item:hover {
    background-color: #f0f0f0;
  }
  
  .list-group-item.active {
   border-right: 5px solid #428777;
    color: #428777;
  }
  </style>
  