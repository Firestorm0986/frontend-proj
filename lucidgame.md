---
title: Lucid Game
layout: default 
permalink: /games/lucidgame
type: pbl
---

# Select what Lucid Model you would like to play on

<div style="text-align: center;">
  <select id="Lucidlist" style="font-size: 20px; padding: 10px;">
    <option value="model1">Lucid Air</option>
    <option value="model2">Lucid Gravity</option>
  </select>
</div>

<script>
    document.getElementById("Lucidlist").onchange = function() {
        var selectedValue = this.value;
    };
</script>

