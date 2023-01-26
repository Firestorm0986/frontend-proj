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

.mytd, th {
  border: 0.5px groove;
  background-color: lightgrey;
  color:

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
</style>
