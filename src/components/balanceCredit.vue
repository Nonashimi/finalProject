<!-- CreditCard.vue -->
<template>
    <div class="credit-card" :style = "{width: width}">
      <div class="card-header">
        <!-- <formProfileImage src="https://thicc-af.mywaifulist.moe/waifus/yuta-okkotsu-sorcery-fight/3DQkg87cFXIigaUzRunm7v3bLXIWTc9BLePplwFu.jpg?class=thumbnail"></formProfileImage> -->
      </div>
      <div class="card-body">
        <div class="card_flex">
            <div class="card_bal">
            <div class="card-number">{{ cardNumber }}</div>
        <div class="card-balance">{{ cardBalance }}</div>
        </div>
        <div class="card_style">
            <div class="circle"></div>
            <div class="circle trns"></div>

        </div>
        </div>
        <div class="balance">
          <div class="">Top Up Balance</div>
          <i class="fa-regular fa-square-plus"></i>
        </div>
        <div class="linest"></div>

        <div class="line"></div>
        <div class="linear"></div>

        <div class="card-info">
          <div class="card-expiry">
            <label>Valid Thru</label>
            <div>{{ expiryDate }}</div>
          </div>
          <div class="card-holder">
            <div class="num">{{ maskedCardNumber }}</div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      cardNumber: String,
      cardBalance: String,
      cardHolderName: String,
      expiryDate: String,
      cardNumb: String,
      top:Boolean,
      width:{
        type:String,
        default:"264px"
      }
    },
   
    computed: {
      maskedCardNumber() {
        let g = this.cardNumb ? `**** **** **** ${this.cardNumb.slice(-4)}` : '';
        return g;
      },
    },
  };
  </script>
  
  <style scoped>
  .credit-card {
    border-radius: 13px;
    overflow: hidden;
    background-color: #428777;
    color: #fff;
    padding: 16px 24px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  .line{
    width:130px;
    height: 130px;
    position: absolute;
   right: -60px;
   top: 50%;
    border: 1px solid #ffffffc6;
    border-radius: 50%;
  }
  .num{
    text-align:right;
  }
  .balance{
    display: flex;
    gap: 20px;
    align-items: center;
    font-size: 18px;
    position: absolute;
    top: 0;
    right: -10px;


  }
  .linest{
    width:200px;
    height: 200px;
    position: absolute;
   right: -90px;
   top: 30%;
    border: 1px solid #ffffffc6;
    border-radius: 50%;
  }
  .linear{
    width:70px;
    height: 70px;
    position: absolute;
   right: -40px;
   top: 80%;
    border: 1px solid #ffffffc6;
    border-radius: 50%;
  }
  .num{
    font-size: 13px;
  }
  .card_flex{
    position: relative;
  }
  .circle{
    width:40px;
    height:40px;
    background-color: #ffffff90;
    border-radius: 50%;
  }
  .card_style{
    position: absolute;
    top: 65px;
    right: -20px;
    display: flex;
  }
  .trns{
    transform: translate(-20px);
  }
  
  .card-header {
    display: flex;
    font-size: 5px;
    justify-content: space-between;
  }
  
  .chip {
    width: 50px;
    height: 30px;
    background: white;
    border-radius: 7px;
  }
  
  .card-logo {
    width: 60px;
  }
  
  .card-body {
    margin-top: 5px;
    position: relative;
  }
  
  .card-number {
    font-size: 14px; 
    margin-bottom: 8px; 
    color: rgb(255, 255, 255);
  }
  .card-balance {
    font-size: 24px; 
  }
  
  .card-info {
    display: flex;
    justify-content: space-between;
    padding-top: 48px;
    align-items: center;
  }
  
  .card-holder,
  .card-expiry {
    flex: 1;
  }
  
  
  label {
    font-size: 10px; 
    opacity: 0.7;
    margin-bottom: 4px; 
  }
  </style>
  