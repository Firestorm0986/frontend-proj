<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/rivianlogo.png" alt="rivianlogo.png" style="width:100%" class="imgMain">
</html>

>>>> # Rivian

>>>> Rivian is an American electric car manufacturing company which builds all-electric, high-end vehicles for many purposes. It was founded in 2009 in Irvine, California. They build SUVs and pickup trucks on "skateboard platforms" which they hope to use on future vehicle types.

>>>> ### Cars in Their Lineup

>>>> Rivian has two cars in their lineup, the R1S and the R1T. The R1S is their luxury, multipurpose SUV, and the R1T is their luxury, multipurpose pickup truck. Deliveries of the R1S and R1T first started in 2021. So far, Rivian has delivered over 21,000 combined units. 

>>>> ## Rivian R1S
<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/Rivian.jpg" alt="Rivian.png" style="width:100%" class="imgMain">
</html>

>>>> The Rivian R1S is their all-electric luxury SUV. The R1S has three rows of seats for a total of 7 passengers. It has a 135 Kilowatt-hour battery, which takes up to 13 hours to charge at 220 Volts. The R1S gets anywhere from 260-315 miles of range, depending on the battery purchased. It can carry up to 7700 pounds of cargo, and it has an all-wheel-drive drivetrain. It can go from 0-60 in three seconds.

>>>> ### R1S Features
>>>> The interior of the R1S has a screen which supports bluetooth connections, CarPlay, and other features. The vehicle has LTE and Wi-Fi connectivity inside, which may allow for connectivity in remote areas. Amazon Alexa is also built-in. There are up to 8 USB ports, 2 12V ports, and 2 120V outlets. Based on customization, leather seats are available. There are many driver-assist features, some of which allow for hands-free driving. 

>>>> ## Rivian R1T
<html>
    <img src="https://firestorm0986.github.io/frontend-proj/images/r1t.jpg" alt="r1t.jpg" style="width:100%" class="imgMain">
</html>

>>>> The Rivian R1T is Rivian's all-electric luxury pickup truck. The R1T has two rows of seats for a total of 5 passengers. Depending on the motor and wheels, the range is anywhere between 260 and 400 miles. It takes up to 13 hours to charge at 220 Volts. The R1T can tow up to 11,000 pounds, and can accelerate from 0-60 in up to three seconds. It sports an All-Wheel-Drive drivetrain.

>>>> ### R1T Features
>>>> The interior of the R1T has a screen which supports bluetooth connections, CarPlay, and other features. The vehicle has LTE and Wi-Fi connectivity inside, which may allow for connectivity in remote areas. Amazon Alexa is also built-in. There are up to 6 USB ports and 4 120V outlets. Based on customization, leather seats are available. There are many driver-assist features, some of which allow for hands-free driving. There are multiple storage spaces in the R1T, which allows for an additional 62 cubic feet of storage space.

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
        <td>Low Center of Gravity, Carbon-fiber material for additional strength, high-strength steel and aluminum, Driver-Assist</td>
        <td>Amazon Alexa Built-in, Bluetooth, Built-in LTE / Wi-FI</td>
        <td>$78,000</td>
    </tr>
    <tr>
        <td>Rivian R1T</td>
        <td>5 People (Two Rows)</td>
        <td>260-400 Miles</td>
        <td>11000 Pounds</td>
        <td>74 Cubic Feet</td>
        <td>Low Center of Gravity, Carbon-fiber material for additional strength, high-strength steel and aluminum, Driver-Assist</td>
        <td>Amazon Alexa Built-in, Bluetooth, Built-in LTE / Wi-FI</td>
        <td>$73,000</td>
    </tr>
</table>
    
<p style="text-align: center; font-size: 54px; color: purple;">Which car best matches your preferences?</p>
<p style="text-align: center; font-size: 50px; color: black;">Click the check boxes below to find out!</p>

<body>
    <p> Select your desired range:</p>
    <label for="range1"><input type="checkbox" id="range1" class="range" value="200 Miles"> 200 Miles </label>
    <label for="range2"><input type="checkbox" id="range2" class="range" value="300 Miles"> 300 Miles </label>
    <label for="range3"><input type="checkbox" id="range3" class="range" value="400 Miles"> 400 Miles </label>
    <label for="range4"><input type="checkbox" id="range4" class="range" value="500 Miles"> 500 Miles </label>
    <button onclick="checkAllOne()"> I do not have a preference </button>
    <p>
        <button id="button1" onclick="getRangeValue()"> Find out which car matches your search</button>
    </p>
    <p> Select your desired seating capacity:</p>
    <label for="seating1"><input type="checkbox" id="seating1" class="seating" value="200 Miles"> 2 People </label>
    <label for="seating2"><input type="checkbox" id="seating2" class="seating" value="300 Miles"> 5 People </label>
    <label for="seating3"><input type="checkbox" id="seating3" class="seating" value="400 Miles"> 7 People </label>
    <button onclick="checkAllTwo()"> I do not have a preference </button>
    <p>
        <button id="button2" onclick="getSeatingValue()"> Find out which car matches your search</button>
    </p>
    <p> Select your desired 0-60 time:</p>
    <label for="zero1"><input type="checkbox" id="zero1" class="zero" value="2 Seconds"> 2 Seconds </label>
    <label for="zero2"><input type="checkbox" id="zero2" class="zero" value="3 Seconds"> 3 Seconds </label>
    <label for="zero3"><input type="checkbox" id="zero3" class="zero" value="4 Seconds"> 4 Seconds </label>
    <label for="zero4"><input type="checkbox" id="zero4" class="zero" value="5 Seconds"> 5 Seconds </label>
    <button onclick="checkAllThree()"> I do not have a preference </button>
    <p>
        <button id="button3" onclick="getZeroValue()"> Find out which car matches your search</button>
    </p>
        <p> Select your desired Price:</p>
    <label for="price1"><input type="checkbox" id="price1" class="price" value="40000"> $40,000 </label>
    <label for="price2"><input type="checkbox" id="price2" class="price" value="60000"> $60,000 </label>
    <label for="price3"><input type="checkbox" id="price3" class="price" value="70000"> $70,000 </label>
    <label for="price4"><input type="checkbox" id="price4" class="price" value="80000"> $80,000 </label>
    <label for="price5"><input type="checkbox" id="price5" class="price" value="100000"> $100,000+ </label>
    <button onclick="checkAllFour()"> I do not have a preference </button>
    <p>
    <button onclick="getPriceValue()"> Find out which car matches your search</button>
    </p>
    <p id="button4"></p>
    <script>
    function checkAllOne() {
        var inputs = document.querySelectorAll('range');
        for (var i = 0; i < inputs.length, i++) {
            inputs[i].checked = true;
        }
    }
    function checkAllTwo() {
        var inputs = document.querySelectorAll('seating');
        for (var j = 0; j < inputs.length, i++) {
            inputs[j].checked = true;
        }
    }
    function checkAllThree() {
        var inputs = document.querySelectorAll('zero');
        for (var k = 0; k < inputs.length, i++) {
            inputs[k].checked = true; 
        }
    }
    function checkAllFour() {
        var inputs = document.querySelectorAll('price');
        for (var l = 0; l < inputs.length, i++) {
            inputs[l].checked = true;
        }
    } 
    function getRangeValue() {
        var l1 = document.getElementById("range1");
        var l2 = document.getElementById("range2");
        var l3 = document.getElementById("range3");
        var l4 = document.getElementById("range4");
        var res = " ";
        if (l1.checked==true){
            document.getElementById("range1").innerHTML = "Tesla Roadster";
        }
    }  

 </script>

</body>
