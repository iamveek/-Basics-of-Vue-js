<template>

<h1> Home screen </h1>
<h1>Email {{email}} </h1>
<h1>Phone {{phone}} </h1>
<h1>Net Worth {{ netWorth()}} </h1>
<h1> Name : {{getData().email}}</h1>
<button v-on:click= "getEvent(' I clicked')" >Click me</button>
<button v-on:dblclick= "getDClick('Doubled')">Click double </button>
<h2 v-on:mousemove= "moveMouse()"> Console Mouse </h2>
<button v-on:click="getCount()"> press</button>
<h2>{{count}}</h2>
 </template>

<script> 

export default {
    name: "Home",
   data(){
     return {
        email: 'afaqk3203@gmail.com',
    phone: '0302',
    netWorth: function(){
     return "20 K";
     
    },
count:0
     }
   },
   methods: {
     getData(){
       return {
         name: "Afaq",
         email: " Azadi @gmail.com",

       
       }
     },
     getCount(){
       this.count= this.count+1;
     },
     getEvent(data){
       alert (data);
     },
     getDClick(data)
     {
       alert (data);
     },
     moveMouse()
     {
       console.warn("Mouse Move")

     },
   }
}

  </script>
  <style scoped> 
  h1{
  color: orange
  }
  
  
  </style>