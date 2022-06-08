<template>
<div>
  <div class="form">
    <h4>
       How many guests your place can accomodate
     </h4>
     <h6>
       Check that you have enough beds to accomodate all your guests comfortably
     </h6>
     <form>
     <label style="margin-right:10px">Guests </label>
      <div class="value-button" id="decrease" onclick="decreaseValue()" value="Decrease Value">-</div>
        <input type="number" id="number" value="10"/>
      <div class="value-button" id="increase" onclick="increaseValue()" value="Increase Value">+</div>
      <div class="form-group">
              <label style="margin-right:10px">How many bedrooms do you use? </label>
              <select id="inputState" class="form-control">
              <option selected>Studios</option>
              <option>...</option>
            </select>
       </div> 
       <p>How many bedrooms do you use?</p>
       <label style="margin-right:10px">Beds </label>
      <div style="border:white" class="value-button" id="decrease" onclick="decreaseValue()" value="Decrease Value" >-</div>
        <input type="number"  id="number" value="1"/>
      <div class="value-button" id="increase" onclick="increaseValue()" value="Increase Value">+</div>
     </form>
  </div>
</div>
</template>
<script>
function increaseValue() {
  var value = parseInt(document.getElementById('number').value, 10);
  value = isNaN(value) ? 0 : value;
  value++;
  document.getElementById('number').value = value;
}

function decreaseValue() {
  var value = parseInt(document.getElementById('number').value, 10);
  value = isNaN(value) ? 0 : value;
  value < 1 ? value = 1 : '';
  value--;
  document.getElementById('number').value = value;
}
</script>
<style>
form {
  width:300px;
  margin:0 auto;
  text-align:center;
  padding-top:50px
}
.value-button {
 display:inline-block;
 border:1px solid green;
 margin:0px;
 width:80px;
 height:40px;
 text-align:center;
 vertical-align:middle;
 padding:11px 0;
 background:#eee;
 -webkit-touch-callout:none;
 -webkit-user-select:none;
 -moz-user-select:none;
 -moz-user-select:none;
 user-select:none;
}
.value-button:hover{
cursor:pointer;
}
form #decrease{
margin-right: -4px;
border-radius:100px;
}
form #increase{
margin-left: -4px;
border-radius:100px;
}
form #input-wrap{
margin:3px;
padding:0px;
}
input#number{
text-align:center;
border:none;
border-top:1px solid #ddd;
border-bottom:1px solid #ddd;
margin:0px;
width:40px;
height:40px
}
input[type=number]::-webkit-inner-spin-
button,
input[type=number]::-webkit-outer-spin-
button {
-webkit-appearance:none;
margin:0;
}
</style>