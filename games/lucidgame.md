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
  const randomKey = Object.keys(percentage_list[randomIndex])[0];
  let randomPercentage;
  if (randomKey === "P00") {
    randomPercentage = "0";
    ans = 588;
  } else if (randomKey === "P10") {
    randomPercentage = "10";
    ans = 529;
  } else if (randomKey === "P20") {
    randomPercentage = "20";
    ans = 471;
  } else if (randomKey === "P30") {
    randomPercentage = "30";
    ans = 412;
  } else if (randomKey === "P40") {
    randomPercentage = "40";
    ans = 353;
  } else if (randomKey === "P50") {
    randomPercentage = "50";
    ans = 294;
  } else if (randomKey === "P60") {
    randomPercentage = "60";
    ans = 235;
  } else if (randomKey === "P70") {
    randomPercentage = "70";
    ans = 176;
  } else if (randomKey === "P80") {
    randomPercentage = "80";
    ans = 118;
  } else if (randomKey === "P90") {
    randomPercentage = "90";
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
  });
</script>
</div>

<script>
  // prepare HTML result container for new output
  const resultContainer = document.getElementById("result");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "https://zesty.nighthawkcodingsociety.com/api/leaderboard/"

  const create_fetch = url + '/create';
  const read_fetch = url + '/';
function read_users() {
  const read_options = {
    method: 'GET',
    headers: {
      'Content-Type': 'application/json'
    },
  };

  fetch('https://example.com/api/leaderboard', read_options)
    .then(response => {
      if (response.status !== 200) {
        throw new Error(`Error fetching leaderboard: ${response.status}`);
      }
      return response.json();
    })
    .then(data => {
      const table = document.createElement('table');
      const headerRow = document.createElement('tr');
      const userHeader = document.createElement('th');
      userHeader.textContent = 'User';
      const scoreHeader = document.createElement('th');
      scoreHeader.textContent = 'Score';
      headerRow.appendChild(userHeader);
      headerRow.appendChild(scoreHeader);
      table.appendChild(headerRow);
      for (const item of data) {
        const row = document.createElement('tr');
        const userCell = document.createElement('td');
        userCell.textContent = item.user;
        const scoreCell = document.createElement('td');
        scoreCell.textContent = item.score;
        row.appendChild(userCell);
        row.appendChild(scoreCell);
        table.appendChild(row);
      }
      resultContainer.innerHTML = '';
      resultContainer.appendChild(table);
    })
    .catch(error => {
      console.error(error);
      const errorMessage = `Error fetching leaderboard: ${error.message}`;
      resultContainer.textContent = errorMessage;
    });
}

</script>

