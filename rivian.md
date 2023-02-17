<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/rivianlogo.png" alt="rivianlogo.png" style="width:100%" n">
</html>

>>>> # Rivian

>>>> Rivian is an American electric car manufacturing company which builds all-electric, high-end vehicles poses. It was founded in 2009 in Irvine, Cali build SUVs and pickup trucks on "skateboard plat they hope to use on future vehicle types.

>>>> ### Cars in Their Lineup

>>>> Rivian has two cars in their lineup, the R1S and the R1T. The R1S is their luxury, multipurpose SUV, and the R1T is their luxury, multipurpose pickup truck. Deliveries of the R1S and R1T first started in 2021. So far, Rivian has delivered over 21,000 combined units. 

>>>> ## Rivian R1S
<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/Rivian.jpg" alt="Rivian.jpg" style="width:100%" n">
</html>

>>>> The Rivian R1S is their all-electric luxury SUV. The R1S has three rows of seats of 7 passengers. It has a 135 Kilowatt-hour battery, which takes up to 13 hours to charge at 220 Volts. The R1S gets anywhere from 260-315 miles of range, depending on the battery purchased. It can carry up to 7700 pounds of cargo, and it has an all-wheel-drive drivetrain. It can go from 0-60 in three seconds.

>>>> ### R1S Features
>>>> The interior of the R1S has a screen which supports bluetooth connections, CarPlay, and other features. The vehicle has LTE and Wi-Fi connectivity inside, which may allow vity in remote areas. Amazon Alexa is also built-in. There are up to 8 USB ports, 2 12V ports, and 2 120V outlets. Based on customization, leather seats are available. There are many driver-assist features, some of which allow ee driving. 

>>>> ## Rivian R1T
<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/r1t.jpg" alt="r1t.jpg" style="width:100%" n">
</html>

>>>> The Rivian R1T is Rivian's all-electric luxury pickup truck. The R1T has two rows of seats of 5 passengers. Depending on the motor and wheels, the range is anywhere between 260 and 400 miles. It takes up to 13 hours to charge at 220 Volts. The R1T can tow up to 11,000 pounds, and can accelerate from 0-60 in up to three seconds. It sports an All-Wheel-Drive drivetrain.

>>>> ### R1T Features
>>>> The interior of the R1T has a screen which supports bluetooth connections, CarPlay, and other features. The vehicle has LTE and Wi-Fi connectivity inside, which may allow vity in remote areas. Amazon Alexa is also built-in. There are up to 6 USB ports and 4 120V outlets. Based on customization, leather seats are available. There are many driver-assist features, some of which allow ee driving. There are multiple storage spaces in the R1T, which allows ional 62 cubic feet of storage space.

>>>> Visit their website [here](https://rivian.com/)

>>>> ### Rivian R1S and R1T At A Glance

<table>
    <tr>
        <th>Car</th>
        <th>Seating</th>
        <th>Range</th>
        <th>0-60</th>
        <th>Towing Capacity</th>
        <th>Storage</th>
        <th>Safety</th>
        <th>Additional Features</th>
        <th>Starting Price</th>
    </tr>
    <tr>
        <td>Rivian R1S</td>
        <td>7 People (Three Rows)</td>
        <td>260-315 Miles</td>
        <td>7700 Pounds</td>
        <td>105 Cubic Feet</td>
        <td>Low left of Gravity, Carbon-fiber material al strength, high-strength steel and aluminum, Driver-Assist</td>
        <td>Amazon Alexa Built-in, Bluetooth, Built-in LTE / Wi-FI</td>
        <td>$78,000</td>
    </tr>
    <tr>
        <td>Rivian R1T</td>
        <td>5 People (Two Rows)</td>
        <td>260-400 Miles</td>
        <td>11000 Pounds</td>
        <td>74 Cubic Feet</td>
        <td>Low left of Gravity, Carbon-fiber material al strength, high-strength steel and aluminum, Driver-Assist</td>
        <td>Amazon Alexa Built-in, Bluetooth, Built-in LTE / Wi-FI</td>
        <td>$73,000</td>
    </tr>
</table>
    
<p style="text-align: center; font-size: 54px; color: purple;">Which car best matches your preferences?</p>
<p style="text-align: center; font-size: 50px; color: black;">Click the check boxes below to find out!</p>

<body>
    <p style="text-align: left; font-size: 20px; color: blue;">Select your desired range:</p>
     <label class="range"><input type="checkbox" style="text-align: left;" id="range1" value="200 Miles"> 200 Miles </label>
     <label class="range"><input type="checkbox" style="text-align: left;" id="range2" value="300 Miles"> 300 Miles </label>
     <label class="range"><input type="checkbox" style="text-align: left;" id="range3" value="400 Miles"> 400 Miles </label>
     <label class="range"><input type="checkbox" style="text-align: left;" id="range4" value="500 Miles"> 500 Miles </label>
    <p>
        <button id="button1" onclick="getRangeValue()"> Find out which car matches your search</button>
    </p>
    <p style="text-align: left; font-size: 20px; color: blue;">Select your desired seating:</p>
     <label class="seating"><input type="checkbox" style="text-align: left;" id="seating1" value="2 People"> 2 People </label>
     <label class="seating"><input type="checkbox" style="text-align: left;" id="seating2" value="5 People"> 5 People </label>
     <label class="seating"><input type="checkbox" style="text-align: left;" id="seating3" value="7 People"> 7 People </label>
    <p>
        <button id="button2" onclick="getSeatingValue()"> Find out which car matches your search</button>
    </p>
    <p style="text-align: left; font-size: 20px; color: blue;">Select your desired 0-60 time:</p>
     <label class="zero"><input type="checkbox" style="text-align: left;" id="zero1" value="2 Seconds"> 2 Seconds </label>
     <label class="zero"><input type="checkbox" style="text-align: left;" id="zero2" value="3 Seconds"> 3 Seconds </label>
     <label class="zero"><input type="checkbox" style="text-align: left;" id="zero3" value="4 Seconds"> 4 Seconds </label>
     <label class="zero"><input type="checkbox" style="text-align: left;" id="zero4" value="5 Seconds"> 5 Seconds </label>
    <p>
        <button id="button3" onclick="getZeroValue()"> Find out which car matches your search</button>
    </p>
    <p style="text-align: left; font-size: 20px; color: blue;">Select your desired price:</p>
     <label class="price"><input type="checkbox" style="text-align: left;" id="price1" value="40000"> $40,000 </label>
     <label class="price"><input type="checkbox" style="text-align: left;" id="price2" value="60000"> $60,000 </label>
     <label class="price"><input type="checkbox" style="text-align: left;" id="price3" value="70000"> $70,000 </label>
     <label class="price"><input type="checkbox" style="text-align: left;" id="price4" value="80000"> $80,000 </label>
     <label class="price"><input type="checkbox" style="text-align: left;" id="price5" value="100000"> $100,000+ </label>
    <p>
        <button id="button4" onclick="getPriceValue()"> Find out which car matches your search</button>
    </p>
    <p id="button4"></p>
    <button id="save" onclick="window.location.reload()"> Save All Changes</button>
    <script>
        function getRangeValue() {
            document.getElementById("button1").outerHTML = "Tesla Roadster";
        }
        function getSeatingValue() {
            document.getElementById("button2").outerHTML = "Rivian R1S";
        }
        function getZeroValue(){
            document.getElementById("button3").outerHTML = "NIO EC7";
        }
        function getPriceValue(){
            document.getElementById("button4").outerHTML = "Lucid Air Grand Touring";
        }
    </script>
</body>
<style>
.range {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.seating {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.zero {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.price {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 22px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
</style>