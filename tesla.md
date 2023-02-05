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
.mytd1 {
    border: 1px solid black;
    height: 60px;

}
.myth1 {
    border: 1px solid black;
}
.mytable1 {
    width: 75%;
    margin: auto;
    text-align: center;
    border-radius: 20px;
    background-color: aliceblue;
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



>>>>>>>#### Bibliography
- [Wikipedia](https://en.wikipedia.org/wiki/Tesla,_Inc.)
- [Tesla.com](https://tesla.com)

>>>>>>>><button name="wikipediabutton" onclick="https://en.wikipedia.org/wiki/Tesla,_Inc.">Wikipedia</button>
>>>>>>>><button name="teslabutton" onclick="https://tesla.com">Tesla.com</button>


>>>>>>>## Live Rankings
<table>
  <thead>
  <tr>
    <th>Car</th>
    <th>Like</th>
    <th>Dislike</th>
  </tr>
  </thead>
  <tbody id="result">
    <!-- javascript generated data -->
  </tbody>
</table>

<script>

  const resultContainer = document.getElementById("result");

  const LIKE = "like";
  const DISLIKE = "dislike";

  const url = "taal.nighthawkcodingteams.cf/api/rankings";
  const like_url = url + "/like/"; 
  const dislike_url = url + "/dislike/";

  const options = {
    method: 'GET',
    mode: 'cors', 
    cache: 'default', 
    credentials: 'omit', 
    headers: {
      'Content-Type': 'application/json'
    },
  };
  const put_options = {...options, method: 'PUT'}; 

  fetch(url, options)
    .then(response => {
      if (response.status !== 200) {
          error('GET API response failure: ' + response.status);
          return;
      }
      response.json().then(data => {
          console.log(data);
          for (const row of data) {
            const tr = document.createElement("tr");
            
            const car = document.createElement("td");
              car.innerHTML = row.id + ". " + row.car;  

            const like = document.createElement("td");
              const like_but = document.createElement('button');
              like_but.id = LIKE+row.id  
              like_but.innerHTML = row.like;  
              like_but.onclick = function () {
                reaction(LIKE, like_url+row.id, like_but.id);  
              };
              like.appendChild(like_but); 

            const dislike = document.createElement("td");
              const dislike_but = document.createElement('button');
              dislike_but.id = DISLIKE+row.id 
              dislike_but.innerHTML = row.dislike; 
              dislike_but.onclick = function () {
                reaction(DISLIKE, dislike_url+row.id, dislike_but.id);  
              };
              dislike.appendChild(dislike_but);  
             
            tr.appendChild(car);
            tr.appendChild(like);
            tr.appendChild(dislike);

            resultContainer.appendChild(tr);
          }
      })
  })
  .catch(err => {
    error(err + " " + url);
  });

  function reaction(type, put_url, elemID) {

    fetch(put_url, put_options)
    .then(response => {
      if (response.status !== 200) {
          error("PUT API response failure: " + response.status)
          return; 
      }
      response.json().then(data => {
          console.log(data);
          if (type === HAHA) 
            document.getElementById(elemID).innerHTML = data.haha;  
          else if (type === BOOHOO) 
            document.getElementById(elemID).innerHTML = data.boohoo; 
          else
            error("unknown type: " + type); 
      })
    })
    .catch(err => {
      error(err + " " + put_url);
    });
    
  }

  function error(err) {
    console.error(err);
    const tr = document.createElement("tr");
    const td = document.createElement("td");
    td.innerHTML = err;
    tr.appendChild(td);
    resultContainer.appendChild(tr);
  }

</script>

>>>>>>>>>>>>## The most liked car is Tesla Model Y with 23 Likes!
>>>>>>>>>>>>## The most disliked car is Rivian R1S with 12 Dislikes!