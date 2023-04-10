<div>
  <img src="{{site.baseurl}}/images/nio.png" alt="main" style="width:100%; position: absolute; z-index: -1;">
  <img src="{{site.baseurl}}/images/nio-second.jpg  " alt="main" class = "image_back" >
  <img src="{{site.baseurl}}/images/back-image2.png" alt="main" class = "image_back2" >
</div>
<div>
  <div class="container2">
    <img src="{{site.baseurl}}/images/ni2-remove.png" alt="main" class = "anima">
  </div>
</div>


<div class = "description-box">
  <h3 class = "body_text"> Description </h3>
  <p class = "body_text"> Nio Inc. is a Chinese multinational automobile manufacturer headquartered in Shanghai, specializing in designing and developing electric vehicles. The company is known for its development of battery-swapping stations for its vehicles, as an alternative to conventional charging stations </p>
  <h3 class = "body_text"> Models </h3>
    <p class = "body_text"> There are a total of 3 models of car with various versions of car in them  </p>
</div>

<table class = "mytable">
  <tr>
    <th>Model</th>
    <th>Version 1</th>
    <th>Version 2</th>
    <th>Version 3</th>
  </tr>
  <tr>
    <td class = "mytd">ET</td>
    <td class = "mytd">et7</td>
    <td class = "mytd">et5</td>
    <td class = "mytd">-</td>
  </tr>
  <tr>
    <td class = "mytd">ES</td>
    <td class = "mytd">es8</td>
    <td class = "mytd">es7</td>
    <td class = "mytd">es6</td>
  </tr>
  <tr>
    <td class = "mytd">EC</td>
    <td class = "mytd">ec7</td>
    <td class = "mytd">ec6</td>
    <td class = "mytd">-</td>
  </tr>
</table>
<div class = "container">
  <div class = "secondary">
    <button class = "mybutton" onclick = "location.href = 'https://www.nio.com/et7'"> ET</button>
    <button class = "mybutton" onclick = "location.href = 'https://www.nio.com/es8'"> ES </button>
    <button class = "mybutton" onclick = "location.href = 'https://www.nio.com/ec7'"> EC</button>
  </div>
  <p class = "body_text2"> click the above links to buy them now </p>
</div>




>>>>>> ### Price and specs

>>>>>>>| Car | O-100 | milage (km) |
| ES7 | 4.9s | 580 |
| ET7 | 3.8s | 1000 |
| ET5 | 4s | 1000|
| ES8 | 4.1s| 900|
| ES6 | 4.7s | 610 |
| EC7 | 3.8s | 940 |
| EC6 | 4.5s | 615 |





<!--- This section is Cascading Style Sheet (CSS) and applies to HTML -->
<style>
/* "row style" is flexible size and aligns pictures in center */
  .image_back{
    position: absolute;
    margin-top:50%;
    z-index: -1;
    width:100%;
  }

  .image_back2{
    position: absolute;
    margin-top:100%;
    z-index: -1;
    width:100%;
  }
  .mytable {
    width:50%;
    margin:auto;
    text-align: center; 
    border-radius: 7px;
    background-color: none;
  }

  .description-box{
    width: 70%;
    margin: auto;
    margin-bottom: 2rem;
    
    border-radius: 5px;
    padding: 5px;
  }

  .body_text{
    margin-left: 3rem; 
    color: white;
  }

  .body_text2{
    margin-left: 3rem; 
    color: white;
    text-align: center;
  }


  .readtable {
    width:70%;
    margin:auto;
    text-align: center;
    background-color: lightgrey;  
    border-radius: 7px;
  }

  .box{
  margin-right: 20%;
  margin-left: 20%;
  height: 100px;
  width: 60%; 
  background-color: white;
  }


  .mytd, th {
    border: 0.5px groove;
    background-color: none;

  }

  .secondary{
    margin-top: 1rem;
    text-align:center;
    margin-bottom: 1rem;
  }

  .mybutton{
    width: 6rem;
    height:2rem;
    border-radius: 5px;
    background-color: lightgrey;
    color:black;
    border: 0px
  }
  .container{
    height: 10%;
    width:100%;
  }

  .container2{
    height: 10%;
    width:100%;

  }

  .image1 {
    width: 100%;
    height:50rem;
  }

  .image1:hover{

  }

  body{
    background-color:darkgrey;
  }


  .anima{
    width: 10%;
    height: 5%;
    
    position: relative;
    animation-name: car;
    animation-duration: 4s;
    margin-left: 10rem;
    margin-right: 10rem;
    animation-iteration-count: infinite;
  }


  @keyframes car {
    0%   { left:0px; top:0px;}
    25%  { left:70%; top:0px;}
    50%  { left:0rem; top:0px;}
  }

  .subbox{
    padding: 2px;
  }

  .createForm{
    text-align: center;
  }
  
  .form-tell{
    text-align: center;
    font-size: 40px;
    margin-top: 5rem;
    color: white;
  }

  .input-boxes{
    width: 50%;
  }

  .form-label{
    font-weight: bold;
    font-size: 20px;
  }

  .form-button{
    width: 6rem;
    height:2rem;
    border-radius: 5px;
    background-color: lightgrey;
    color:black;
    border: 0px;
    font-size: 20px;
    font-weight: bold;
  }

  .form-box{
      
      padding: 2%;
      
      width: 75%;
      border-radius: 5px;
      background-color: bisque;
      margin: auto;
      margin-bottom: 5rem;
  }

  .read-button{
      width: auto;
      margin: auto;
      align-self: center;
  }

  * {box-sizing: border-box;}
  body {font-family: Verdana, sans-serif;}
  .mySlides {display: none;}
  img {vertical-align: middle;}

  /* Slideshow container */
  .slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
  }

  /* Caption text */
  .text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
  }

  /* Number text (1/3 etc) */
  .numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
  }

  /* The dots/bullets/indicators */
  .dot {
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
  }

  .active {
  background-color: #717171;
  }

  /* Fading animation */
  .fade {
  animation-name: fade;
  animation-duration: 1.5s;
  }

  @keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
  }

  /* On smaller screens, decrease text size */
  @media only screen and (max-width: 300px) {
  .text {font-size: 11px}
  }
</style>

<div class = "secondary">
<button id = "read_button" type = "button" onclick="read_users()"  class = "read-button"> Generate a Fact </button>
</div>
<table class = "readtable">
  <thead>
  <tr>
    <th>Car Fact</th>
    <th>industry fact</th>
    <th>id</th>

  </tr>
  </thead>
  <tbody id="result">
    <!-- javascript generated data -->
  </tbody>
</table>


<p class = "form-tell">Add Your Own Fact</p>

<div class = "form-box">
  <form action="javascript:create_fact()" class = "createForm">
      <p><label class = "form-label">
          Car Fact:
          <input class = "input-boxes" type="text" industry="car" id="car" required>
      </label></p>
      <p><label class = "form-label">
          industry fact:
          <input class = "input-boxes" type="text" industry="industry" id="industry" required>
      </label></p>
      <p>
          <button class = "form-button">Create</button>
      </p>
  </form>
</div>
<div class = "form-box">
  <form action = "javascript:delete_fact()" class = "createForm">
    <p><label class = "form-label">
      ID to delete:
      <input class = "input-boxes" type = "text" industry="id" id = "id" required>
    </label></p>
    <p>
      <button class = "form-button">Delete</button>
    </p>
  </form>
</div>

<div class="slideshow-container">

  <div class="mySlides fade">
    <div class="numbertext">1 / 3</div>
    <img src="{{site.baseurl}}/images/slide-image2.jpg" style="width:100%">
    <div class="text">Caption Text</div>
  </div>
  
  <div class="mySlides fade">
    <div class="numbertext">2 / 3</div>
    <img src="{{site.baseurl}}/images/slide-image3.jpg" style="width:100%">
    <div class="text">Caption Two</div>
  </div>
  
  <div class="mySlides fade">
    <div class="numbertext">3 / 3</div>
    <img src="{{site.baseurl}}/images/slide-image1.jpg" style="width:100%">
    <div class="text">Caption Three</div>
  </div>
  
  </div>
  <br>
  
  <div style="text-align:center">
    <span class="dot"></span> 
    <span class="dot"></span> 
    <span class="dot"></span> 
  </div>



<script>
  // prepare HTML result container for new output
  const resultContainer = document.getElementById("result");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "http://127.0.0.1:8086/api/facts/" 

  const create_fetch = url + '/create';
  const read_fetch = url + '/';
  const delete_fetch = url + '/delete';

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


  function create_fact(){
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
    // Fetch API call to the database to create a new fact
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
      id: document.getElementById("id").value,
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
  fetch(delete_fetch, requestOptions)
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