---
title: Game Charging Info
layout: default 
permalink: /info/charge
type: pbl
---
<div class = "secondary">
</div>
<table class = "readtable">
  <thead>
  <tr>
    <th>Car</th>
    <th>Charge Times</th>
    <th>ID</th>

  </tr>
  </thead>
  <tbody id="result">
    <!-- javascript generated data -->
  </tbody>
</table>


<p class = "form-tell">Let us know if you drive an electric car!</p>

<div class = "form-box">
  <form action="javascript:create_user()" class = "createForm">
      <p><label class = "form-label">
          Car:
          <input class = "input-boxes" type="text" industry="car" id="car" required>
      </label></p>
      <p><label class = "form-label">
          Time it takes to charge:
          <input class = "input-boxes" type="text" industry="industry" id="industry" required>
      </label></p>
      <p>
          <button class = "form-button">Submit</button>
      </p>
  </form>
</div>

<script>
  // prepare HTML result container for new output
  const resultContainer = document.getElementById("result");
  // prepare URL's to allow easy switch from deployment and localhost
  const url = "https://zesty.nighthawkcodingsociety.com/api/facts/"

  const create_fetch = url + '/create';
  const read_fetch = url + '/';
</script>