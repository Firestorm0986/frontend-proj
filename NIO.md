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
>>>>>>> There are a total of 3 models of car with various veriosns of car in them 

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

<style>
  .inputform{
    text-align:center;
  }
</style>



<h1 class = "mytext"> Random Fact Generator </h1>
<button  class = "mytext" > Generate A Fact </button>
<br> 
<br> 

<p id = "read" onclick="fact_generate()"> The random facts will display here </p>
<p id = "read2"> </p>
  


<form class = "inputform" id = "create_form">
  <input type = "text" id = "car_query" placeholder = "the car fact">
  <input type = "text" id = "industry_query" placeholder = "The industry fact">


  <button type = "submit"> Submit </button>
</form>


<script>
  /*
    const apiurl = "http://172.29.204.228:8086/"
    window.onload = APIsync()
    
    function APIsync(){
        fetch(apiurl)
        .then(response => {
            response.json().then(data => {
                console.log(data)
                console.log(data.car)
               
                
        })
    })
    }
  */
  function fact_generate(){
      document.getElementById("read").innerHTML = "/ My name "; 
  } 
  
  
  
  
  
  
  
  
  
  /*
  const car = document.getElementById('car_query')
  const industry = document.getElementById('industry_query')
  const form = document.getElementById('create_car')
 
  // prepare HTML read container for new output
  const readContainer = document.getElementById("read");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "http://localhost:8086/api/facts"
  const create_fetch = url + '/create';
  const read_fetch = url + '/';

  // Load facts on page entry
  read_facts();


  // Display User Table, data is fetched from Backend Database
  function read_facts() {
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
            
            car.innerHTML = errorMsg;
            industry.innerHTML = errorMsg;
            return;
        }
        // valid response will have json data
        response.json().then(data => {
            console.log(data);
            for (let row in data) {
              console.log(data[row]);
              add_row(data[row]);
            }
        })
    })


    // catch fetch errors (ie ACCESS to server blocked)
    


  function create_fact(){
    //Validate Password (must be 6-20 characters in len)
    //verifyPassword("click");
    const body = {
        car: document.getElementById("car_query").value,
        industry: document.getElementById("industry_query").value,  
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
          
          car.innerHTML = errorMsg;
          industry.innerHTML = errorMsg;
          return;
        }
        // response contains valid read
        response.json().then(data => {
            console.log(data);
            //add a table row for the new/created userid
            add_row(data);
        })
    })
  }

  function add_row(data) {
    
  

    // obtain data that is specific to the API
    car.innerHTML = data.car; 
    industry.innerHTML = data.industry; 

    // add HTML to container
  }
</script>