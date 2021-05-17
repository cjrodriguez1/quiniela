<template>
    <div class="container">
    <h3>Quiniela:</h3>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Local</th>
          <th scope="col">Resultado</th>
          <th scope="col">Visitante</th>
          <th scope="col">Isael</th>
          <th scope="col">Angel</th>
          <th scope="col">Charlie</th>
          <th scope="col">Omar</th>
          <th scope="col">Hector</th>
          <th scope="col">Rosas</th>
          <th scope="col">Ishar</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" v-bind:key="user.id"> 
          <td>{{user.local}}</td>
          <th scope="row">{{user.resultado}}</th>
          <td>{{user.visitante}}</td> 
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.isael}}</div>
            <div v-else-if="user.isael === user.resultado" style="background-color:#00FF00">{{user.isael}}</div>
            <div v-else-if="user.isael !== user.resultado" style="background-color:#FF0000">{{user.isael}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.angel}}</div>
            <div v-else-if="user.angel === user.resultado" style="background-color:#00FF00">{{user.angel}}</div>
            <div v-else-if="user.angel !== user.resultado" style="background-color:#FF0000">{{user.angel}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.charlie}}</div>
            <div v-else-if="user.charlie === user.resultado" style="background-color:#00FF00">{{user.charlie}}</div>
            <div v-else-if="user.charlie !== user.resultado" style="background-color:#FF0000">{{user.charlie}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.omar}}</div>
            <div v-else-if="user.omar === user.resultado" style="background-color:#00FF00">{{user.omar}}</div>
            <div v-else-if="user.omar !== user.resultado" style="background-color:#FF0000">{{user.omar}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.hector}}</div>
            <div v-else-if="user.hector === user.resultado" style="background-color:#00FF00">{{user.hector}}</div>
            <div v-else-if="user.hector !== user.resultado" style="background-color:#FF0000">{{user.hector}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.rosas}}</div>
            <div v-else-if="user.rosas === user.resultado" style="background-color:#00FF00">{{user.rosas}}</div>
            <div v-else-if="user.rosas !== user.resultado" style="background-color:#FF0000">{{user.rosas}}</div>
          </td>
          <td>
            <div v-if="user.resultado === ''" style="background-color:#FFFFFF">{{user.ishar}}</div>
            <div v-else-if="user.ishar === user.resultado" style="background-color:#00FF00">{{user.ishar}}</div>
            <div v-else-if="user.ishar !== user.resultado" style="background-color:#FF0000">{{user.ishar}}</div>
          </td>
        </tr>
      </tbody>
    </table> 
  </div> 
</template>
<script>
 // import axios from 'axios';

  export default {
    name: 'Users',
    data() {
      return {
        gcolor: "blue",
        rcolor: "red",
        users: [
    {
     "local": "Toluca",
     "resultado": "L",
     "visitante": "Cruz Azul",
     "isael": "V",
     "angel": "L",
     "charlie": "V",
     "omar": "V",
     "hector": "V",
     "rosas": "E",
     "ishar": "V",
    },
    {
     "local": "Atlas",
     "resultado": "L",
     "visitante": "Puebla",
     "isael": "L",
     "angel": "V",
     "charlie": "E",
     "omar": "E",
     "hector": "L",
     "rosas": "V",
     "ishar": "L",
    },
     {
     "local": "Pachuca",
     "resultado": "L",
     "visitante": "America",
     "isael": "E",
     "angel": "V",
     "charlie": "E",
     "omar": "E",
     "hector": "V",
     "rosas": "V",
     "ishar": "E",
    },
    {
     "local": "Santos",
     "resultado": "L",
     "visitante": "Monterrey",
     "isael": "L",
     "angel": "E",
     "charlie": "L",
     "omar": "L",
     "hector": "L",
     "rosas": "V",
     "ishar": "L",
    },
     {
     "local": "Cruz Azul",
     "resultado": "L",
     "visitante": "Toluca",
     "isael": "L",
     "angel": "E",
     "charlie": "L",
     "omar": "L",
     "hector": "L",
     "rosas": "L",
     "ishar": "L",
    },
    {
     "local": "Puebla",
     "resultado": "L",
     "visitante": "Atlas",
     "isael": "E",
     "angel": "L",
     "charlie": "E",
     "omar": "L",
     "hector": "V",
     "rosas": "E",
     "ishar": "E",
    },
     {
     "local": "America",
     "resultado": "L",
     "visitante": "Pachuca",
     "isael": "L",
     "angel": "L",
     "charlie": "L",
     "omar": "L",
     "hector": "L",
     "rosas": "L",
     "ishar": "L",
    },
    {
     "local": "Monterrey",
     "resultado": "E",
     "visitante": "Santos",
     "isael": "L",
     "angel": "L",
     "charlie": "V",
     "omar": "L",
     "hector": "V",
     "rosas": "L",
     "ishar": "L",
    },
     {
     "local": "Pachuca",
     "resultado": "",
     "visitante": "Cruz Azul",
     "isael": "",
     "angel": "",
     "charlie": "",
     "omar": "",
     "hector": "",
     "rosas": "",
     "ishar": "",
    },
     {
     "local": "Santos",
     "resultado": "",
     "visitante": "Puebla",
     "isael": "",
     "angel": "",
     "charlie": "",
     "omar": "",
     "hector": "",
     "rosas": "",
     "ishar": "",
    },
     {
     "local": "Cruz Azul",
     "resultado": "",
     "visitante": "Pachuca",
     "isael": "",
     "angel": "",
     "charlie": "",
     "omar": "",
     "hector": "",
     "rosas": "",
     "ishar": "",
    },
     {
     "local": "Puebla",
     "resultado": "",
     "visitante": "Santos",
     "isael": "",
     "angel": "",
     "charlie": "",
     "omar": "",
     "hector": "",
     "rosas": "",
     "ishar": "",
    },
   
    
  ]
      };
    },
    created: function() {
      var myArray = this.users;
      myArray.forEach(element => {
        console.log(element);
      });
      /*axios
        //.get('https://jsonplaceholder.typicode.com/users')
        .get('../assets/allUsers.json')
        .then(res => {
          this.users = res.data;
        })*/
    }
  }
</script>
<style>
  h3 {
    margin-bottom: 5%;
  }
  
</style>