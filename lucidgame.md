---
title: Lucid Game
layout: default
description: description 
permalink: /games/lucidgame
image: /images/dart.png
type: pbl
---

# lucid test

<select id="myList">
  <option value="item1">Item 1</option>
  <option value="item2">Item 2</option>
  <option value="item3">Item 3</option>
  <option value="item4">Item 4</option>
</select>

<script>
    document.getElementById("myList").onchange = function() {
        var selectedValue = this.value;
    };
</script>
