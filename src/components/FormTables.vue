<template>
    <div>
      <table>
        <thead>
          <tr>
            <th v-for = "item in thText" :key  ="item">
              {{ item }}
            </th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="user in users" :key="user.id">
            <td><miniCredit :color ="user.color" width ="150px" height="45px"></miniCredit></td>
            <td>{{ user.name }}</td>
            <td>{{ user.email }}</td>
            <td>{{ user.number }}</td>
            <td>{{ user.nameCard }}</td>
            <td><i class="fa-solid fa-ellipsis"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  import miniCredit from './miniCredit.vue';
  export default {
    components:{
    miniCredit
    },
    props:{
       users:{
        type :Array,
        default: () => [
        { color:"#428777", name: 'Primary', email: 'ABC Bank' , number: "**** **** **** 1234", nameCard:"Tony Soap"},
        { color:"#f0ca43", name: 'Secondary', email: 'ABC Bank',number: "**** **** **** 5678" ,nameCard:"Tony Soap"},
        { color:"#ee4444", name: 'Secondary', email: 'ABC Bank',number: "**** **** **** 9012" ,nameCard:"Tony Soap"},
        { color:"#9babc5", name: 'Secondary', email: 'ABC Bank',number: "**** **** **** 3456" ,nameCard:"Tony Soap"},

        // Add more user data as needed
      ],
       },
       thText:{
        type:Array,
        default: ()=>["Card" , "Card Type" , "Bank", "Card Number", "Namein",""],

        
       }
   
  },
  data(){
    return{
    }
  }
}
  </script>
  
  
  <style scoped>
  /* Add your table styling here */
  table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
  }

  
  th, td {
    padding: 16px 8px;
    text-align: left;
  }
  i{
    color: #adbacf;
  }

  
  th {
    border-bottom: 1px solid #e6eaf0;
    color: #c0cada;
    font-weight: 500;
  }
  </style>
  