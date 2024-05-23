<template>
  <div class="">
    <div class="title">
      <spendTitle name = "Transaction Overview"></spendTitle>
    
      <div class="inOut">
        <DropDownButton label = "This Week" color = "#afbcd0"></DropDownButton>
        <div class="pp">
          <div class="inOu">
  <div class="circle" :style ="{backgroundColor: color[0].one}"></div>
<formText color="#afbcd0" label ="Income" size = "14px"></formText>
</div>
<div class="inOu">
  <div class="circle" :style ="{backgroundColor: color[0].two}"></div>
<formText color="#afbcd0" label ="Outcome" size = "14px"></formText>
</div>
        </div>

      </div>
    </div>
  <div class="vert">
    <div class="vertical-counter">
      <div>2000</div>
      <div>1500</div>
      <div>1000</div>
      <div>500</div>
      <div>0</div>
      
    </div>
    <div class="day">
      <div class="bar">
      <div class="bar_tips" v-for="(item, index) in arr" :key="index" >
        <div class="bar_tip"  :style="{ height: `${item.one }%`, left: `${(index * 70+20)}px`, backgroundColor: color[0].one }"></div>
        <div class="bar_tip2" :style="{ height: `${item.two }%`, left: `${(index * 70+40)}px`, backgroundColor: color[0].two }"></div>
      </div>
      
    </div>
      <div class="days-of-week">
      <span>M</span>
      <span>T</span>
      <span>W</span>
      <span>T</span>
      <span>F</span>
      <span>S</span>
      <span>S</span>
    </div>
    </div>
   
      
   
  </div>
   
  </div>
  
  </template>
  
  <script>
  import spendTitle from './spendTitle.vue';
  import DropDownButton from './DropDownButton.vue';
  import formText from './formText.vue';
  export default {
    components:{
      spendTitle,
      DropDownButton,
      formText

    },
    props: {
      arr: {
        type: Array,
        default: () => [
     {one:27.5 , two:22.5},
     {one:60, two:45},
     {one:20 ,two:25 },
     {one:8  ,two: 5 },
     {one: 40 ,two: 36},
     {one:25 , two:23},
     {one:74,two: 69}
        ],
      },
    },
    
    data() {
      return {
        color: [
          {one:"#428777", two:"#f0ca43"}
        ],
      };
    },
    mounted() {
      this.transform();
    },
    methods: {
      transform() {
        let bar = document.querySelector(".bar");
        for (let i = 0; i < bar.children.length; i++) {
          let li = bar.children[i];
          li.style.left = `${i * bar.scrollWidth / (this.arr.length - 1)}px`;
        }
      },
    },
  };
  </script>
  
  <style scoped>
  .bar {
    position: relative;
    width: 500px;
    height:350px ;
   
  }
  .pp{
    display: flex;
    gap: 20px;
  }
  .vertical-counter {
    height: 100%;
}

.inOu{
  display: flex;
  gap: 3px;
  align-items: center;
}
.circle{
  width: 5px;
  height: 5px;
  border-radius: 50%;
}
.inOut{
display: flex;
 justify-content: space-between;
}

.vertical-counter div{
  margin: 10px 0 60px;
  text-align: right;
  color: #afbcd0;
  font-size: 15px;
}
.vert{
  display: flex;
}
   
.days-of-week {
  display: flex;
  justify-content: space-between;
  color: #afbcd0;
}

span {
  flex-grow: 1;
  text-align: center;
}
   
  
  .bar_tip , .bar_tip2 {
    width: 10px;
    position: absolute;
    bottom: 0;
    transition: height 0.5s ease; /* добавлено анимированное изменение высоты */
  }
  </style>
  