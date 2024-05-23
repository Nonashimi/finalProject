<template>
<div class="alll">
<button @click="clickButton" id="0">Monthly</button>
<button @click="clickButton" id="1">Weekly</button>
<button @click="clickButton" id="2" class = "a">Today</button>
    
</div>
</template>

<script>
export default{
data(){
    return{
        active :2,
    }
},

methods:{
    clickButton(e){
      this.active = e.target.id;
      let all = document.querySelector(".alll");
      for(let i  = 0;i<all.children.length;i++){
        if(i==e.target.id){
            all.children[i].classList.add("a");
        }else{
            all.children[i].classList.remove("a");

        }
      }
    }
}

}
</script>

<style scoped>
button{
    padding: 10px 13px;
    background-color: rgb(201, 199, 199);
    border: none;
    color: #fff;
  transition: all .3s;
  border-radius: 30px;
}
.a{
    background-color: #428777;
}
.all{
    font-size: 20px;
    font-family: 'Roboto', sans-serif;
}


</style>