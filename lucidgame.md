---
title: Lucid Game
layout: default 
permalink: /games/lucidgame
type: pbl
---

<p style="text-align: center; font-size: 50px; color: darkblue;">Please select what Lucid Model you would like to play on</p>

<br>
<div style="text-align: center;">
  <select id="Lucidlist" style="font-size: 40px; padding: 10px;">
    <option style="font-size: 30px;" value="">Models</option>
    <option style="font-size: 30px;" value="model1">Lucid Air</option>
    <option style="font-size: 30px;" value="model2">Lucid Gravity (Predict)</option>
  </select>
</div>
<br>

<script>
    document.getElementById("Lucidlist").onchange = function() {
        var selectedValue = this.value;
    };
</script>

<script>
  const person = {
    firstName: "John",
    lastName: "Doe", 
    age: 50,
    status: "marketing contact"
  };
  person["firstName"];/*returns the value John"*/
  person.firstName;/*Also returns the value "John"*/
</script>

<script>
  const functions = {
    lucidAir: ,
    lucidGravity: ,
  };
</script>