---
layout: default
title: Locatie
permalink: /locatie.html
---

<div class="row">
	<div class="small-12 columns">

		<h1> Locatie </h1>
		<div class="flex-video">
		<iframe width="600" height="450" frameborder="0" style="border:0" id="map"
src="https://www.google.com/maps/embed/v1/directions?origin=helchteren%20kruispunt&destination=Zandstraat%2029%2C%20Houthalen-Helchteren%2C%20Belgium&key=AIzaSyChAbfCxkoLZcilvMM9Tok2kMQcNikoNLw"></iframe>
		</div>
	</div>
</div>
<div class="row">
	<div class="small-12 columns">
	<form id="richting">
		<label>Voer hier je adres in:
			<input type="text" name="address" id="address">
			<input type="submit" class="button" id="route" value="Bereken route">
		</label>
	</form>
	</div>
</div>

</div>

<script>
var form = document.getElementById("richting");
form.addEventListener("submit", function(e){
	e.preventDefault();
	var key = "AIzaSyC26Ly-xwS3GwGhL-sHNQvGCjRB7D3TTzQ";
	var origin = encodeURIComponent(document.getElementById("address").value);
	
	var src = "https://www.google.com/maps/embed/v1/directions?origin=" + origin + "&destination=Zandstraat%2029%2C%20Houthalen-Helchteren%2C%20Belgium&key=" + key;
	document.getElementById("map").src = src;
});
</script>