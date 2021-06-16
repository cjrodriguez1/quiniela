<template>
    <div class="container">
    <h3>Audiovisuales:</h3>
    <table class="table">
      <thead>
        <tr>
          <th scope="col">Servicio</th>
          <th scope="col">Usuario</th>
          <th scope="col">Contraseña</th>
           <th scope="col">Proveedor</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" v-bind:key="user.id"> 
          <th scope="row">{{user.local}}</th>
          <td>{{user.resultado}}</td>
          <td>{{user.visitante}}</td> 
          <td>{{user.proveedor}}</td> 
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
     "local": "Netflix",
     "resultado": "aerosas@icloud.com",
     "visitante": "clave1",
     "proveedor": "Rosas",
     "angel": "L",
     "charlie": "V",
     "omar": "V",
     "hector": "V",
     "rosas": "E",
     "ishar": "V",
    },
    {
     "local": "Disney+",
     "resultado": "guyonthebeach8@yahoo.com",
     "visitante": "clave2",
     "proveedor": "Rosas",
     "angel": "V",
     "charlie": "E",
     "omar": "E",
     "hector": "L",
     "rosas": "V",
     "ishar": "L",
    },
     {
     "local": "Hulu",
     "resultado": "guyonthebeach8@yahoo.com",
     "visitante": "clave2",
     "proveedor": "Rosas",
     "angel": "V",
     "charlie": "E",
     "omar": "E",
     "hector": "V",
     "rosas": "V",
     "ishar": "E",
    },
    {
     "local": "ESPN+",
     "resultado": "guyonthebeach8@yahoo.com",
     "visitante": "clave2",
     "proveedor": "Rosas",
     "angel": "E",
     "charlie": "L",
     "omar": "L",
     "hector": "L",
     "rosas": "V",
     "ishar": "L",
    },
     {
     "local": "Blue to go",
     "resultado": "ishar.sajid@hotmail.com",
     "visitante": "ishar_18",
     "proveedor": "PRIshar",
     "angel": "E",
     "charlie": "L",
     "omar": "L",
     "hector": "L",
     "rosas": "L",
     "ishar": "L",
    },
    {
     "local": "HBOMax",
     "resultado": "carlos.csci@gmail.com",
     "visitante": "clave1*",
     "proveedor": "Charlie",
     "angel": "L",
     "charlie": "E",
     "omar": "L",
     "hector": "V",
     "rosas": "E",
     "ishar": "E",
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