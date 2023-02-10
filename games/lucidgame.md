---
title: Lucid Game
layout: default 
permalink: /games/lucidgame
type: pbl
---

<p style="text-align: center; font-size: 50px; color: darkblue;">Today, you will be driving the Lucid Air</p>
<div style="text-align:center;">
  <a style="font-size: 40px; color: lightblue; display:inline-block; width:100%;" href="{{site.baseurl}}/lucidinfo">Learn About Lucid</a>
</div>

<div id="gridContainer">
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
</div>
<img id="draggableImage" src="dart.png" draggable="true">

<style>
  #gridContainer {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    width: 300px;
    height: 300px;
  }

  .grid-cell {
    border: 1px solid black;
    width: 100px;
    height: 100px;
  }

  #draggableImage {
    width: 100px;
    height: 100px;
  }
</style>

<script>
  const gridContainer = document.getElementById("gridContainer");
  const draggableImage = document.getElementById("draggableImage");

  draggableImage.addEventListener("dragstart", function(event) {
    event.dataTransfer.setData("text/plain", event.target.id);
  });

  gridContainer.addEventListener("dragover", function(event) {
    event.preventDefault();
  });

  gridContainer.addEventListener("drop", function(event) {
    event.preventDefault();
    const data = event.dataTransfer.getData("text/plain");
    const element = document.getElementById(data);
    event.target.appendChild(element);
  });
</script>