---
title: Game Charging Info
layout: default 
permalink: /info/charge
type: pbl
---
<div class = "secondary">
<button id = "read_button" type = "button" onclick="read_users()"  class = "read-button"> Show Charging Times for Cars</button>
</div>
<table class = "readtable">
  <thead>
  <tr>
    <th>Car</th>
    <th>Charge Times</th>
    <th>ID</th>

  </tr>
  </thead>
  <tbody id="result">
  </tbody>
</table>


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
      method: 'GET', // *GET, POST, PUT, DELETE, etc.
      mode: 'cors', // no-cors, *cors, same-origin
      cache: 'default', // *default, no-cache, reload, force-cache, only-if-cached
      credentials: 'omit', // include, *same-origin, omit
      headers: {
        'Content-Type': 'application/json'
      },
    };
    fetch(read_fetch, read_options)
      // response is a RESTful "promise" on any successful fetch
      .then(response => {
        // check for response errors
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
        // valid response will have json data
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
    // catch fetch errors (ie ACCESS to server blocked)
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
      
    id.innerHTML = data.id; 
    

    // add HTML to container
    tr.appendChild(car);
    tr.appendChild(chargetime);
    
    tr.appendChild(id);
    

    resultContainer.appendChild(tr);
  }

  function create_fact(){
    //Validate Password (must be 6-20 characters in len)
    //verifyPassword("click");
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

    // URL for Create API
    // Fetch API call to the database to create a new user
    fetch(create_fetch, requestOptions)
      .then(response => {
        // trap error response from Web API
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
        // response contains valid result
    })
  }

  function delete_fact(){
  //Validate Password (must be 6-20 characters in len)
  //verifyPassword("click");
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
  // Fetch API call to the database to create a new user
  fetch(create_fetch, requestOptions)
    .then(response => {
      // trap error response from Web API
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
      // response contains valid result
  })
  }
  /// New for slideshow

  let slideIndex = 0;
  showSlides();

</script>