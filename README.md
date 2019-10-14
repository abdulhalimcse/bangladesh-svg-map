# bangladesh-svg-map
Bangladesh SVG Map

## About Bangladesh SVG MAP

It is simple SVG MAP. We can use this map to follow some data format. 

## Install
Clone or Download the bangladesh-svg-map and see it.

Or 

Follow below step

## Step 1

Add CSS 

```html
<link rel="stylesheet" href="bangladesh-map/bd-map.css">
```

Add jQuery

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script> 
```

Add MAP JS library

```html
<script src="bangladesh-map/bd-svg.js"></script>
<script src="bangladesh-map/bd-map.js"></script>
```

## Step 2

Please use CSS class "map" and id "changeSvgMap" (You can use CSS id like your choice)

```html
<div class="map" id="changeSvgMap"></div>
```

## Step 3

```html
<script> 
$(document).ready(function() {
	var regionsOfBangladesh = {
		"bangladesh": [
			{
				"region_name": "Rangpur",
				"region_id": "rangpurDivision",
				"area": 800,
				"population": 9794525
			},
			{
				"region_name": "Dhaka",
				"region_id": "dhakaDivision",
				"area": 700,
				"population": 5769750
			},
			{
				"region_name": "Rajshahi",
				"region_id": "rajshahiDivision",
				"area": 600,
				"population": 5557276
			},
			{
				"region_name": "Sylhet",
				"region_id": "sylhetDivision",
				"area": 500,
				"population": 4999932
			},
			{
				"region_name": "Mymensingh",
				"region_id": "mymensinghDivision",
				"area": 400,
				"population": 4881756
			},
			{
				"region_name": "Barishal",
				"region_id": "barisalDivision",
				"area": 300,
				"population": 4377487
			},
			 {
				"region_name": "Khulna",
				"region_id": "khulnaDivision",
				"area": 200,
				"population": 4374052
			},
			{
				"region_name": "Chittagong",
				"region_id": "chittagongDivision",
				"area": 100,
				"population": 4050803
			}
  ]};	
  
  var regionKey = 'bangladesh';
  var title = 'Bangladesh MAP';

	$("#changeSvgMap").generateMap({
		'title' : title,
		'regionKey' : regionKey,
		'regionData' : regionsOfBangladesh
	});
  
});
</script>

```




