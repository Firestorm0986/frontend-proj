---
title: Game Charging Info
layout: default 
permalink: /info/charge
type: pbl
---

<script>
  // prepare HTML result container for new output
  const resultContainer = document.getElementById("result");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "https://zesty.nighthawkcodingsociety.com/api/facts/"

  const create_fetch = url + '/create';
  const read_fetch = url + '/';

  // Load users on page entry
  const read_button = document.getElementById("read_button");
  


  // Display User Table, data is fetched from Backend Database
  function read_users() {
    // prepare fetch options
    
    const read_options = {
      method: 'GET', // *GET, POST, PUT, DELETE, etc.
      mode: 'cors', // no-cors, *cors, same-origin
      cache: 'default', // *default, no-cache, reload, force-cache, only-if-cached
      credentials: 'omit', // include, *same-origin, omit
      headers: {
        'Content-Type': 'application/json'
      },
    };

    // fetch the data from API
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
    const industry = document.createElement("td");
    
    const id = document.createElement("td");
    
  

    // obtain data that is specific to the API
    car.innerHTML = data.car; 
    industry.innerHTML = data.industry; 
      
    id.innerHTML = data.id; 
    

    // add HTML to container
    tr.appendChild(car);
    tr.appendChild(industry);
    
    tr.appendChild(id);
    

    resultContainer.appendChild(tr);
  }


  function create_user(){
    //Validate Password (must be 6-20 characters in len)
    //verifyPassword("click");
    const body = {
        car: document.getElementById("car").value,
        industry: document.getElementById("industry").value,
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
  /// New for slideshow

  let slideIndex = 0;
  showSlides();

  function showSlides() {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";  
  }
  slideIndex++;
  if (slideIndex > slides.length) {slideIndex = 1}    
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
  setTimeout(showSlides, 2000); // Change image every 2 seconds
  }
</script>