<template>
  <v-container grid-list-md text-xs-center>
    <v-flex align-center align-content-center>
      <v-text-field name="name" v-model="name" label="identificador"></v-text-field>
      <v-btn color="success" @click="makeRequest()">Buscar Usuario</v-btn>
      <h1>{{httpRequest}}</h1>
      <p style="white-space: pre-line;">{{ userData }}</p>
    </v-flex>
  </v-container>
</template>
<style>
</style>

<script>
import axios from "axios";

export default {
  data() {
    return {
      texto: "RESULTADO JSON",
      userData: [],
      name: "",
      httpRequest: "Petición HTTP"
    };
  },
  created: function() {
    //let y = this.makeRequest();
    //console.log(y);
  },
  methods: {
    makeRequest: function() {
      var that = this;
      let result;

      axios
        .get("http://localhost:3000/api/" + that.name)
        .then(function(response) {
          // handle success
          //console.log(response.data);
          result = response.data;
          //console.log(result);
          that.userData = response.data;
        })
        .catch(function(error) {
          // handle error
          console.log(error);
        })
        .finally(function() {
          // always executed
        });
      that.httpRequest = "http://localhost:3000/api/" + that.name;
    }
  }
};
</script>

