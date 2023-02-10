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

<div style="text-align:center;">

<button style="text-align: center; font-size: 50px; color: darkgreen;" id="playButton">Play</button>

<div id="gridContainer" style="display: none;">
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
<img id="draggableImage" src="dart.png" draggable="true" style="display: none;">

<style>
  #gridContainer {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    width: 900px;
    height: 900px;
    background-color: black;
    margin: 0 auto;
  }

  .grid-cell {
    border: 1px solid white;
    width: 300px;
    height: 300px;
  }

  #draggableImage {
    width: 200px;
    height: 200px;
  }
</style>

<script>
  const playButton = document.getElementById("playButton");
  const gridContainer = document.getElementById("gridContainer");
  const draggableImage = document.getElementById("draggableImage");

  playButton.addEventListener("click", function() {
    gridContainer.style.display = "grid";
    draggableImage.style.display = "block";
  });

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

</div>