<template>
<div class="">
<header class ="header">
    <div class="container">
        <div class="space"></div>
        <!-- <formDrawers>
            <div class="icon">
        <formIconsVue size = "35px" color  ="#198568" iconType ="bank"></formIconsVue>
      <div class="iconName">Bilpay</div>
    </div>
        </formDrawers> -->

     
<div class="nav">
 <formSearchBar placeholder="Search..."></formSearchBar>
 <LabelAndBadges class="lll" label = '<i class="fa-regular fa-bell"></i>' ></LabelAndBadges>
 <LabelAndBadges class="lll" label = '<i class="fa-regular fa-envelope"></i>' ></LabelAndBadges>
 <formIconsVue iconType="settings"></formIconsVue>
 <formListVue title = "Olzhas Yergali" text="Admin"></formListVue>
</div>
    </div>
   
</header>
</div>

</template>

<script>
import formIconsVue from './formIcons.vue';
import LabelAndBadges from './LabelAndBadges.vue';
import formSearchBar from './formSearchBar.vue';
import formListVue from './formList.vue';
// import formDrawers from './formDrawers.vue';
export default{
    props:{

    },
    data(){

    },
    components:{
     formIconsVue,
     LabelAndBadges,
     formSearchBar,
     formListVue,
    //  formDrawers
    }
}

</script>

<style scoped>
.header{
    background-color: #fcfbfb;
    
}
.space{
    width:258px;
    height: 10px;
    background-color: #fcfbfb;
}
.container{
    display: flex;
    align-items: center;
    gap: 80px;
    width: 1400px;
    margin: 0 auto;
    padding: 20px 0;
}
.icon{
    display: flex;
   gap: 10px;
   cursor: pointer;
}


.iconName{
    color: #111111;
    font-size: 25px;
    font-weight: 800;
    margin-top: 6%;
}
.nav{
    display: flex;
    width: 80%;
   align-items: center;
   gap: 50px;
}

</style>