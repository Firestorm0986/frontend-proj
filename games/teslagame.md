---
title: Tesla Game
layout: default
permalink: /games/teslagame
type: pbl
---

<p style="text-align: center; font-size: 50px; color: darkblue;">Today, you will be driving the Tesla Model Y</p>
<div style="text-align:center;">
  <a style="font-size: 40px; color: lightblue; display:inline-block; width:100%;" href="https://firestorm0986.github.io/frontend-proj/tesla">Learn About Tesla</a>
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
<img id="draggableImage" src="https://firestorm0986.github.io/frontend-proj/images/teslacar.webp" draggable="true" style="display: none;">
<div id="question" style="display: none;">
  <p style="text-align: center; font-size: 30px; color: darkblue;">How long will it take to charge the Tesla Model Y?</p>
  <br>
<form>
  <label style="width: 50px; height: 50px; margin: 0 auto; color: blue;" for="input">Enter your prediction (in minutes): </label>
  <br>
  <input type="number" id="input" name="input" style="margin-bottom: 20px;">
  <br>
  <button type="submit" id="submitButton" style="text-align: center; font-size: 25px; color: lightblue; display: none; margin: 20px auto 0;">Submit</button>
  <br>
  <a id="Info" style="font-size: 40px; color: lightblue; display:inline-block; width:100%; display: none;" href="{{site.baseurl}}/info/charge">Get information about charging times</a>
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
    {"00": "455"},
    {"10": "409"},
    {"20": "364"},
    {"30": "318"},
    {"40": "273"},
    {"50": "227"},
    {"60": "182"},
    {"70": "136"},
    {"80": "91"},
    {"90": "45"}
  ];
  const randomIndex = Math.floor(Math.random() * percentage_list.length);
  const randomKey = Object.keys(percentage_list[randomIndex])[0];
  let randomPercentage;
  if (randomKey === "00") {
    randomPercentage = "0";
    ans = 455;
  } else if (randomKey === "10") {
    randomPercentage = randomKey;
    ans = 409;
  } else if (randomKey === "20") {
    randomPercentage = randomKey;
    ans = 364;
  } else if (randomKey === "30") {
    randomPercentage = randomKey;
    ans = 318;
  } else if (randomKey === "40") {
    randomPercentage = randomKey;
    ans = 273;
  } else if (randomKey === "50") {
    randomPercentage = randomKey;
    ans = 227;
  } else if (randomKey === "60") {
    randomPercentage = randomKey;
    ans = 182;
  } else if (randomKey === "70") {
    randomPercentage = randomKey;
    ans = 136;
  } else if (randomKey === "80") {
    randomPercentage = randomKey;
    ans = 91;
  } else if (randomKey === "90") {
    randomPercentage = randomKey;
    ans = 45;
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
    scoreText.textContent = "You scored: " + score + " points, the best score you can get is 1000";
    submitButton.parentNode.insertBefore(scoreText, submitButton.nextSibling);
    submitButton.style.display = "none";
    const Info = document.getElementById("Info");
    Info.style.display = "block";
  });
</script>
</div>

