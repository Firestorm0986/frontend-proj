---
title: Game Charging Info
layout: default 
permalink: /info/charge
type: pbl
---
<div class = "secondary">
<button id = "read_button" type = "button" onclick="read_users()"  class = "read-button"> Show The Different Charging Times for Electric Cars</button>
</div>

<table class = "readtable">
  <thead>
  <tr>
    <th>Car</th>
    <th>Charge Times</th>
  </tr>
  </thead>
  <tbody id="result">
  </tbody>
</table>

<style>
.readtable {
  background-color: #e0ffe0;
}
</style>

<p class = "form-tell">Let us know if you drive an electric car!</p>

<div class = "form-box">
  <form action="javascript:create_user()" class = "createForm">
      <p><label class = "form-label">
          Car:
          <input class = "input-boxes" type="text" chargetime="car" id="car" required>
      </label></p>
      <p><label class = "form-label">
          Time it takes to charge:
          <input class = "input-boxes" type="text" chargetime="chargetime" id="chargetime" required>
      </label></p>
      <p>
          <button class = "form-button">Submit</button>
      </p>
  </form>
</div>

<script>
    const resultContainer = document.getElementById("result");
    const url = "https://zesty.nighthawkcodingsociety.com/api/charges/"
    const create_fetch = url + '/create';
    const read_fetch = url + '/';
    const read_button = document.getElementById("read_button");
    function read_users() {
      const read_options = {
      method: 'GET', 
      mode: 'cors', 
      cache: 'default', 
      credentials: 'omit', 
      headers: {
        'Content-Type': 'application/json'
      },
    };
    fetch(read_fetch, read_options)
   
      .then(response => {

        if (response.status !== 200) {
            const errorMsg = 'Database read error: ' + response.status;
            console.log(errorMsg);
            const tr = document.createElement("tr");
            const td = document.createElement("td");
            td.innerHTML = errorMsg;
            tr.appendChild(td);
            resultContainer.appendChild(tr);
            return;
        }
 
        response.json().then(data => {
            console.log(data);
            length = data.length;
            number = Math.floor(Math.random() * length );
            for (let row in data) {
              console.log(data[row]);
              
              add_row(data[number]);
              break;
            }
        })
    })
    .catch(err => {
      console.error(err);
      const tr = document.createElement("tr");
      const td = document.createElement("td");
      td.innerHTML = err;
      tr.appendChild(td);
      resultContainer.appendChild(tr);
    });
  }
function add_row(data) {
    const tr = document.createElement("tr");
    const car = document.createElement("td");
    const chargetime = document.createElement("td");

    const id = document.createElement("td");
    car.innerHTML = data.car; 
    chargetime.innerHTML = data.chargetime; 
    

    tr.appendChild(car);
    tr.appendChild(chargetime);

    resultContainer.appendChild(tr);
}


  function create_fact(){
    const body = {
        car: document.getElementById("car").value,
        chargetime: document.getElementById("chargetime").value,
    };
    const requestOptions = {
        method: 'POST',
        body: JSON.stringify(body),
        headers: {
            "content-type": "application/json",
            'Authorization': 'Bearer my-token',
        },
    };

    fetch(create_fetch, requestOptions)
      .then(response => {
        if (response.status !== 200) {
          const errorMsg = 'Database create error: ' + response.status;
          console.log(errorMsg);
          const tr = document.createElement("tr");
          const td = document.createElement("td");
          td.innerHTML = errorMsg;
          tr.appendChild(td);
          resultContainer.appendChild(tr);
          return;
        }
    })
  }

  function delete_fact(){

  const body = {
      car: document.getElementById("car").value,
      chargetime: document.getElementById("chargetime").value,
  };
  const requestOptions = {
      method: 'DELETE',
      body: JSON.stringify(body),
      headers: {
          "content-type": "application/json",
          'Authorization': 'Bearer my-token',
      },
  };
  // URL for Create API
  fetch(create_fetch, requestOptions)
    .then(response => {
      if (response.status !== 200) {
        const errorMsg = 'Database create error: ' + response.status;
        console.log(errorMsg);
        const tr = document.createElement("tr");
        const td = document.createElement("td");
        td.innerHTML = errorMsg;
        tr.appendChild(td);
        resultContainer.appendChild(tr);
        return;
      }
  })
  }
  let slideIndex = 0;
  showSlides();

</script>