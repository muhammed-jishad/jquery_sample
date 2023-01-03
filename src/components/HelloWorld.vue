<template>
 <p>If you click on the "Hide" button, I will disappear.</p>

<button id="hide">Hide</button>
<button id="show">Show</button>

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
export default {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

