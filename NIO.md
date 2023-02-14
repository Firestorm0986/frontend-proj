<div>
  <img src="{{site.baseurl}}/images/nio.png" alt="main" style="width:100%">
</div>

<div>
  <div class="container2">
    <img src="{{site.baseurl}}/images/ni2-remove.png" alt="main" class = "anima">
  </div>
</div>

>>>>>>## NIO
>>>>>>> __Nio Inc.__ is a Chinese multinational automobile manufacturer headquartered in Shanghai, specializing in designing and developing electric vehicles. The company is known for its development of battery-swapping stations for its vehicles, as an alternative to conventional charging stations

>>>>>>### Modles
>>>>>>> There are a total of 3 models of car with various versions of car in them 

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
</div>

>>>>>>> - Click the above buttons to take you to the newest version of that modle of car.


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
  .mytable {
    width:50%;
    margin:auto;
    text-align: center;
    background-color: lightgrey;  
    border-radius: 7px
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
    background-color: lightgrey;

  }

  .secondary{
    margin-top: 1rem;
    text-align:center;
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
    background:lightgrey;
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
    background-color: lightgrey;
    position: relative;
    animation-name: car;
    animation-duration: 4s;
    margin-left: 10rem;
    margin-right: 10rem;
    animation-iteration-count: infinite;
  }


  @keyframes car {
    0%   {background-color:lightgrey; left:0px; top:0px;}
    25%  {background-color:lightgrey; left:70%; top:0px;}
    50%  {background-color:lightgrey; left:0rem; top:0px;}
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
</style>


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

<form action="javascript:create_user()" class = "createForm">
    <p><label class = "form-label">
        User ID:
        <input class = "input-boxes" type="text" industry="car" id="car" required>
    </label></p>
    <p><label class = "form-label">
        industry:
        <input class = "input-boxes" type="text" industry="industry" id="industry" required>
    </label></p>
    <p>
        <button class = "form-button">Create</button>
    </p>
</form>

<script>
  // prepare HTML result container for new output
  const resultContainer = document.getElementById("result");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "http://localhost:8086/api/facts"

  const create_fetch = url + '/create';
  const read_fetch = url + '/';

  // Load users on page entry
  read_users();


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
  
</script>