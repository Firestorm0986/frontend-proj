<style>

.mytd {
    height: 80px;
    width: 160px;
    text-align: center;
    vertical-align: middle;
    border: 1px solid black;
    
}
.myth{
    border: 1px solid black;
    height: 30px;
}
.mytable1 {
    width: 85%;
    margin: auto;
    text-align: center;
    background-color: aliceblue;
    border: 1px solid black;
}
img {
    width: 90%;
    height: 275%;
    object-fit: contain;
}

.mytable {
  width:70%;
  margin:auto;
  text-align: center;
  background-color: lightgrey;  
  border-radius: 20px
}
.mytext {
    font-weight: bolder;
}
 td {
  border: 1px solid black;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>


<div class = "img1">
    <img src = "{{site.baseurl}}/images/tesla.jpg" style = "width:100%">
</div>

>>>>>>># Tesla
>>>>>>>>## Background Info
>>>>>>>>>**Tesla** is an American multinational company that focuses on automotives and clean energy. Its headquarters are in Austin, Texas and its current ceo is **Elon Musk**. The purpose of Tesla is to help transition society to sustainable transport and energy through its use of electric vehicals and solar panels.

>>>>>>>>## Products
>>>>>>>>>Tesla produces a variety of goods and products - more than just cars
- Electric vehicles - cars and trucks
- Battery Energy Storage - Powerwall, Megapack
- Solar Panels
- Solar roof tiles
- Charging Stations

>>>>>>>>## Money/Popularity
>>>>>>>>> Tesla is the world's most valuable automaker as of 2022 and is also one of the world's most valuable companies.
- In 2021, Tesla had the most worldwide sales of electric vehicles - battery and plug-in
    - 21% of batter market an 14% of plug-in market
- Subsidary (Tesla Energy) is a major installer of photovoltaic systems and is one of the largest global suppliers of battle energy storage systems
- Tesla annual revenue for 2021 was $53.8 billion
- Tesla's net worth has also passed $1 trillion, being the sixth company in the U.S. to do so


>>>>>>>>## Cars


<table class = "mytable">
    <tr>
        <th class = "myth">Car</th>
        <th class = "myth">Release Date</th>
        <th class = "myth">Facts/Features</th>
        <th class = "myth">Picture</th>
    </tr>
    <tr>
        <td class = "mytd">Tesla Model S</td>
        <td class = "mytd">June 22, 2012</td>
        <td class = "mytd">5 door sedan<BR>First Electric vehicle to top monthly sales<BR>Time Magazine's Best 25 inventions of 2012<BR>Bestselling plug-in car worldwide for 2015-16<BR>EPA Range of 402 miles<BR>Top speed of 149 mph<BR>670 hp with 3.1 s 0-60 mph</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-model-s.jpg"  /></td>
    </tr>
    <tr>
        <td class = "mytd">Tesla Model X</td>
        <td class = "mytd">September 2015</td>
        <td class = "mytd">Mid-size crossover SUV<BR>Developed from full-sized sedan platform of Model S<BR>Falcon-wing design for back doors<BR>Ranked 7th among world's bestselling plug-in cars 2016<BR>EPA Range of 348 miles<BR>3.8 s 0-60 mph with 670 hp<BR>Top speed of 155 mph</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-model-x.jpg"></td>
    </tr>
    <tr>
        <td class = "mytd">Tesla Model 3</td>
        <td class = "mytd">July 28, 2017</td>
        <td class = "mytd">4 door fastback sedan<BR>Over 325,000 reservations after unveiling<BR>World's best selling electric car in history<BR>Global sales passed 1 million<BR>3.1 s 0-60 mph<BR>EPA range of 315 miles<BR>Dual Motor All-Wheel Drive<BR>15" Center Touchscreen</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-model-3.jpg"></td>
    </tr>
    <tr>
        <td class = "mytd">Tesla Model Y</td>
        <td class = "mytd">March 13, 2020</td>
        <td class = "mytd">Compact crossover utility vehicle<BR>Shares many components with Model 3<BR>EPA Range of 326 miles<BR>3.5s 0-60 mph with top speed of 155 mph<BR>Dual Motor All-Wheel Drive<BR>15" Center Touchscreen</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-model-y.jpg"></td>
    </tr>
    <tr>
        <td class = "mytd">Tesla Semi</td>
        <td class = "mytd">December 2022</td>
        <td class = "mytd">All-electric Class 8 semi-trailer truck<BR>2 variants: 300 miles and 500 miles range<BR>4 independent electric motors<BR>Set of hardware sensors<BR>Soon-to-come autopilot mode</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-semi.jpg" ></td>
    </tr>
    <tr>
        <td class = "mytd">Tesla Roadster</td>
        <td class = "mytd">Late 2023</td>
        <td class = "mytd">Range of 620 miles<BR>200 kilo-watt hours batter pack<BR>1.9 s 0-60 mph and 4/2 s 0-100 mph<BR>Top speed of over 250 mph<BR>Cold air thrusters and three electric motors<BR>All-wheel drive and torque vectoring during cornering</td>
        <td class = "mytd"><img src = "{{site.baseurl}}/images/tesla-roadster.jpg"></td>
    </tr>
</table>


>>>>>>>## Live Rankings

<table class="mytable1" id="cars_table">
  <thead>
  <tr>
    <th class="myth">ID</th>
    <th class="myth">Car</th>
    <th class="myth">Like</th>
    <th class="myth"># of Likes</th>
    <th class="myth">Delete</th>
  </tr>
  </thead>
  <tbody class="mytd" id="result">
    <!-- javascript generated data -->
  </tbody>
</table>

<p><center>Add your Own Car!</center></p>

<form action="javascript:create_car()"><center>
    <p><label>
        Car
        <input type="text" name="car" id="car" required>
    </label></p>
    <p>
        <button id="add_car" onclick='create_car()'>Create</button>
    </p>
</center></form>

<script>
  const resultContainer = document.getElementById("result");
  const url = "https://zesty.nighthawkcodingsociety.com/api/schemas"
  const create_fetch = url + '/create';
  const read_fetch = url + '/';
  const delete_fetch = url + '/delete';
  const update_fetch = url + '/update';


  // Load users on page entry
  read_cars();


  // Display User Table, data is fetched from Backend Database
  function read_cars() {
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
            for (let row in data) {
              console.log(data[row]);
              add_row(data[row]);
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

  function create_car(){
    //Validate Password (must be 6-20 characters in len)
    //verifyPassword("click");
    const body = {
        car: document.getElementById("car").value,
        like: 0,

    };
    const requestOptions = {
        method: 'POST',
        mode: 'cors',
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
        response.json().then(data => {
            console.log(data);
            //add a table row for the new/created userid
            add_row(data);
        })
    })
  }
  
  function delete_car(car_id){

    const body = {
        id: car_id,

    };

    fetch(url, {
      method: 'DELETE',
    })
      .then((response) => response.json())
      response.json().then(data => {
        console.log(data);
        add_row(data);
      })
  };
  const clearCars = async () => {
	const list = await fetch(url, {
		method: "DELETE",
	}).then((r) => r.json());
  };

const removecar = async () => {
	const todo = await fetch(url, {
		method: "DELETE",
		headers: {
			"Content-Type": "application/json",
		},
		body: JSON.stringify({ id:1 }),
	}).then((r) => r.json());


  };

    /*const requestOptions = {
        method: 'DELETE',
        mode: 'cors',
        body: JSON.stringify(body),
        headers: {
            'content-type': 'application/json',
            'Authorization': 'Bearer my-token',
        },
        body: JSON.stringify(body),

    };

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
          response.json().then(data => {
            console.log(data);
            //add a table row for the new/created userid
            add_row(data);
        })
    })*/

  function like_car(car_id, num_like) {
    const body = {
        id: car_id,
        like: num_like,

    };
    const requestOptions = {
        method: 'PATCH',
        mode: 'cors',
        credentials: 'omit',
        body: JSON.stringify(body),
        headers: {
            "content-type": "application/json",
            'Authorization': 'Bearer my-token',
            
        },
    };
    

    // URL for Create API
    // Fetch API call to the database to create a new user
    fetch(update_fetch, requestOptions)
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
        response.json().then(data => {
            console.log(data);
            //add a table row for the new/created userid
            add_row(data);
        })
    })
  }

  function add_row(data) {
    const tr = document.createElement("tr");
    tr.class="mytd"
    const car = document.createElement("td");
    const id = document.createElement("td");
    const col2 = document.createElement("td");
    const col4 = document.createElement("td");
    const like_button = document.createElement('input');
    like_button.type = "button";
    like_button.value = "Like";
    like_button.onclick = function() {like_car(data.id, data.like+1)};
    const num_like = document.createElement('td');
    const delete_button = document.createElement('input');
    delete_button.type = "button";
    delete_button.value = "Delete";
    delete_button.onclick = function() {delete_car(data.id)};

    col2.appendChild(like_button);
    col4.appendChild(delete_button);
  
    // obtain data that is specific to the API
    car.innerHTML = data.car;
    id.innerHTML = data.id;
    num_like.innerHTML = data.like;

    // add HTML to container
    tr.appendChild(id);
    tr.appendChild(car);
    tr.appendChild(col2);
    tr.appendChild(num_like);
    tr.appendChild(col4);

    //resultContainer.appendChild(td);
    resultContainer.appendChild(tr);
  }
</script>
