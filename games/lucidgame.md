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
<br>
<div style="text-align:center;">

<button style="text-align: center; font-size: 50px; color: darkgreen;" id="playButton">Play</button>

<div id="gridContainer" style="display: none;">
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div id="parkHere" style="color: white;" class="grid-cell">Park Here</div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
  <div class="grid-cell"></div>
</div>
<img id="draggableImage" src="https://firestorm0986.github.io/frontend-proj/images/lucidcar.webp" draggable="true" style="display: none;">
<div id="question" style="display: none;">
  <p style="text-align: center; font-size: 30px; color: darkblue;">How long will it take to charge the Lucid Air?</p>
  <textarea style="width: 200px; height: 20px; margin: 0 auto;"></textarea>
</div>

<style>
  #gridContainer {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    width: 666px;
    height: 666px;
    background-color: black;
    margin: 0 auto;
  }

  .grid-cell {
    border: 1px solid white;
    width: 222px;
    height: 222px;
  }

  #draggableImage {
    width: 200px;
    height: 200px;
    margin: 0 auto;
  }
</style>

<script>
  const playButton = document.getElementById("playButton");
  const gridContainer = document.getElementById("gridContainer");
  const draggableImage = document.getElementById("draggableImage");
  const question = document.getElementById("question");
  const parkHere = document.getElementById("parkHere");

  playButton.addEventListener("click", function() {
    gridContainer.style.display = "grid";
    draggableImage.style.display = "block";
  });

  draggableImage.addEventListener("dragstart", function(event) {
    event.dataTransfer.setData("text", event.target.id);
  });

  parkHere.addEventListener("dragover", function(event) {
    event.preventDefault();
  });
  parkHere.addEventListener("drop", function(event) {
  event.preventDefault();
  const data = event.dataTransfer.getData("text");
  event.target.appendChild(document.getElementById(data));
  question.style.display = "block";
  const percentage_list = [
    {"P00": "588"},
    {"P10": "529"},
    {"P20": "471"},
    {"P30": "412"},
    {"P40": "353"},
    {"P50": "294"},
    {"P60": "235"},
    {"P70": "176"},
    {"P80": "118"},
    {"P90": "59"}
  ];
  const randomIndex = Math.floor(Math.random() * percentage_list.length);
  const randomPercentage = Object.values(percentage_list[randomIndex])[0];
  const message = document.createElement("p");
  message.textContent = "How long will it take to charge the car from " + randomPercentage + "%";
  question.insertBefore(message, question.firstChild);
});

</script>
</div>
