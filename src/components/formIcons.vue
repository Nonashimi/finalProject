<template>
<div class="">
    <div class="img" :style="{color:color , fontSize:size}" v-html="getIcons()">
    </div>
</div>
</template>

<script>
export default{
    props:{
        size:{
          type:String,
          default:"20px"
        },
        color:{
            type:String,
            default:"gray",
        },
        iconType:String,
        
    },
    data(){
        return{
            settings:`<i class="fa-solid fa-gear"></i>`,
            date: `<i class="fa-solid fa-calendar-days"></i>`,
            clock: `<i class="fa-solid fa-clock"></i>`,
           hippo:`<i class="fa-solid fa-hippo"></i>`,
           bank:`<i class="fa-solid fa-piggy-bank"></i>`,
           up:`<i class="fa-solid fa-arrow-trend-up"></i>`,
           down:`<i class="fa-solid fa-arrow-trend-down"></i>`,
           transfer: `<i class="fa-solid fa-right-left"></i>`,
           send: `<i class="fa-solid fa-share-from-square"></i>`
 
        }
    },
    methods:{
        getIcons(){
            switch (this.iconType) {
        case "settings":
          return this.settings;
        case "bank":
          return this.bank;
        case "clock":
          return this.clock;
        case "hippo":
          return this.hippo;
          case "up":
          return this.up;
          case "down":
          return this.down;
          case "transfer":
          return this.transfer;
          case "send":
          return this.send;
        default:
          return this.settings;
      }
        }
    }
}
</script>

<style scoped>
.red{
    color: red;
}

</style>