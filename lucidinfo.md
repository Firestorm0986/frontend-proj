---
title: Lucid Info
layout: default 
permalink: /lucidinfo
type: pbl
---

## Lucid
> Founded by Bernard Tse, Sam Weng, and Sheaupyng Lin, Lucid Motors, Inc. was created in 2007, originally "focused on building electric vehicle batteries and powertrains for other vehicle manufacturers". Eventually the company moved to all electric car manufacturing after many began to invest. 

### 2024 Lucid Gravity
> **Overview:** 
- Duel electric motors
- All wheel drive
- Performance-oriented Grand Touring trim

![]({{site.baseurl}}/images/gravity.png "test")

| Model | Estimated Price | Horsepower |
| - | - | - |
| Pure | $90,000 | 1,000 |
| Touring | $110,000 | ~1,100 |
| Grand Touring | $140,000 | ~1,100 |
| Grand Touring Performance | $170,000 | ~1,100 |
| Sapphire | $250,000 | 1,200 |


### Lucid Air
> **Overview:**
- Lucid's "main", most popular car with 
- In 2018, the Lucid prototype gained media popularity by "smoking" other electric car models such as those made by Tesla
- Many upgraded versions have been produced up until they started production on their new, unreleased 2024 Lucid Gravity 

| Lucid Air Model | EPA Range | Horsepower | Price |
| - | - | - | - |
| Dream Edition Range (19″ wheels) | 520 mi. | 933 | $169,000 |
| Dream Edition Range (21″ wheels) | 481 mi. | 933 | $169,000 |
| Dream Edition Performance (19″ wheels) | 471 mi. | 1111 | $169,000 |
| Dream Edition Performance (21″ wheels) | 451 mi. | 1111 | $169,000 |
| Grand Touring (19″ wheels) | 516 mi. | 800 | $139,000 |
| Grand Touring (21″ wheels) | 469 mi. | 800 | $139,000 |
| Touring | 406 mi. | 620 | $95,000 |
| Pure | 406 mi. | 480 | $77,400 |

<button onclick="myFunction()">Dream Edition</button>
<script>
function myFunction() {
  var x = document.createElement("IMG");
  x.setAttribute("src", "dreamedition.png");
  x.setAttribute("width", "304");
  x.setAttribute("height", "228");
  x.setAttribute("alt", "image");
  document.body.appendChild(x);
}
</script>

<button onclick="myFunction()">Touring</button>
<script>
function myFunction() {
  var y = document.createElement("IMG");
  y.setAttribute("src", "air.png");
  y.setAttribute("width", "304");
  y.setAttribute("height", "228");
  y.setAttribute("alt", "image");
  document.body.appendChild(y);
}
</script>

<button onclick="myFunction()">Pure</button>
<script>
function myFunction() {
  var z = document.createElement("IMG");
  z.setAttribute("src", "pure.png");
  z.setAttribute("width", "304");
  z.setAttribute("height", "228");
  z.setAttribute("alt", "image");
  document.body.appendChild(z);
}
</script>

<br>

<html>
  <head>
    <style>
      table {
        border-collapse: collapse;
      }
      td {
        width: 50px;
        height: 50px;
        border: 1px solid black;
        text-align: center;
      }
      #piece {
        width: 48px;
        height: 48px;
        background-color: red;
        position: absolute;
      }
    </style>
  </head>
  <body>
    <table>
      <tr>
        <td id="cell-1"></td>
        <td id="cell-2"></td>
        <td id="cell-3"></td>
        <td id="cell-4"></td>
        <td id="cell-5"></td>
      </tr>
      <tr>
        <td id="cell-6"></td>
        <td id="cell-7"></td>
        <td id="cell-8"></td>
        <td id="cell-9"></td>
        <td id="cell-10"></td>
      </tr>
      <tr>
        <td id="cell-11"></td>
        <td id="cell-12"></td>
        <td id="cell-13"></td>
        <td id="cell-14"></td>
        <td id="cell-15"></td>
      </tr>
      <tr>
        <td id="cell-16"></td>
        <td id="cell-17"></td>
        <td id="cell-18"></td>
        <td id="cell-19"></td>
        <td id="cell-20"></td>
      </tr>
      <tr>
        <td id="cell-21"></td>
        <td id="cell-22"></td>
        <td id="cell-23"></td>
        <td id="cell-24"></td>
        <td id="cell-25"></td>
      </tr>
    </table>
    <div id="piece"></div>
  </body>
</html>
