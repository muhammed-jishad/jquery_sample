<template>
 <p>If you click on the "Hide" button, I will disappear.</p>

<button id="hide">Hide</button>
<button id="show">Show</button>
<button @click="getdata">hh</button>
</template>
<script>

import $ from 'jquery'
$(document).ready(function(){
  $("#hide").click(function(){
    $("p").hide();

  });
  $("#show").click(function(){
    $("p").show();
  });
});
export default {
  methods:{
     async getdata() {
      const dat=await fetch('https://sandbox.redch.in/schedule/1', {
    headers: {
      'Access-Control-Allow-Origin': '*',
      "Access-Control-Allow-Methods":"DELETE, POST, GET, OPTIONS",
        'content-type': 'application/json',
        'accept': 'application/json',
        'X-MOVIE-CLICKS-CLIENT-ID': 'hilite',
        'authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpYXQiOjE2NjY4NDUyNDAsImlzcyI6ImxvY2FsaG9zdCIsImV4cCI6MTY2Njg1MjQ0MCwidXNlcklkIjoiMSJ9.Y8aPjxOp07BTgN7a319F0sf5NGSisRrUfQ3FjQ0cRXw'
    }
});
console.log(dat);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

