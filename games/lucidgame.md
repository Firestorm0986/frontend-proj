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
<a id="Info" style="font-size: 40px; color: lightblue; display:inline-block; width:100%; display: none;" href="{{site.baseurl}}/info/charge">Get information about charging times</a>
<div id="question" style="display: none;">
  <p style="text-align: center; font-size: 30px; color: darkblue;">How long will it take to charge the Lucid Air?</p>
  <br>
<form>
  <label style="width: 50px; height: 50px; margin: 0 auto; color: blue;" for="input">Enter your prediction (in minutes): </label>
  <br>
  <input type="number" id="input" name="input" style="margin-bottom: 20px;">
  <br>
  <button type="submit" id="submitButton" style="text-align: center; font-size: 25px; color: lightblue; display: none; margin: 20px auto 0;">Submit</button>
</form>
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
    {"00": "588"},
    {"10": "529"},
    {"20": "471"},
    {"30": "412"},
    {"40": "353"},
    {"50": "294"},
    {"60": "235"},
    {"70": "176"},
    {"80": "118"},
    {"90": "59"}
  ];
  const randomIndex = Math.floor(Math.random() * percentage_list.length);
  const randomKey = Object.keys(percentage_list[randomIndex])[0];
  let randomPercentage;
  if (randomKey === "00") {
    randomPercentage = "0";
    ans = 588;
  } else if (randomKey === "10") {
    randomPercentage = randomKey;
    ans = 529;
  } else if (randomKey === "20") {
    randomPercentage = randomKey;
    ans = 471;
  } else if (randomKey === "30") {
    randomPercentage = randomKey;
    ans = 412;
  } else if (randomKey === "40") {
    randomPercentage = randomKey;
    ans = 353;
  } else if (randomKey === "50") {
    randomPercentage = randomKey;
    ans = 294;
  } else if (randomKey === "60") {
    randomPercentage = randomKey;
    ans = 235;
  } else if (randomKey === "70") {
    randomPercentage = randomKey;
    ans = 176;
  } else if (randomKey === "80") {
    randomPercentage = randomKey;
    ans = 118;
  } else if (randomKey === "90") {
    randomPercentage = randomKey;
    ans = 50;
  }
  const message = document.createElement("p");
  message.textContent = "The car is at " + randomPercentage + "%";
  question.insertBefore(message, question.firstChild);
  });

  const submitButton = document.getElementById("submitButton");
  submitButton.style.display = "block";
  submitButton.addEventListener("click", function(event) {
    event.preventDefault();
    const input = parseInt(document.getElementById("input").value);
    if (isNaN(input)) {
      alert("Please enter a valid number.");
      message.textContent = "Please enter a number";
      return;
    }
    const score = 1000 - Math.abs(ans - input);
    const scoreText = document.createElement("p");
    scoreText.textContent = "You scored: " + score + " points";
    submitButton.parentNode.insertBefore(scoreText, submitButton.nextSibling);
    submitButton.style.display = "none";
    const Info = document.getElementById("Info");
    Info.style.display = "block";
  });
</script>
</div>

