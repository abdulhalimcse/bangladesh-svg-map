# bangladesh-svg-map
Bangladesh SVG Map

## About Bangladesh SVG MAP

It is simple SVG MAP. We can use this map to follow some data format. 

## Install
Clone or Download the bangladesh-svg-map and see it.

Or 

Follow below step

## Step 1

Add CSS (find it bangladesh-map folder)

```html
<link rel="stylesheet" href="bangladesh-map/bd-map.css">
```

Add jQuery

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script> 
```

Add MAP JS library (find it bangladesh-map folder)

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

Generate Map id will be same your div id. 
You have to send three data in generateMap. which are below
1. title ( it will be map title)
2. regionKey ( it will be 'bangladesh' for all division map. You can see district map With All upazilla, key will be district name with District keyword. Exp. rangpurDistrict)
3. regionsOfBangladesh ( it will be json data. You have to generate JSON data below format)


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


## Step 4 (Full Sample)
We can show bangladesh map using this library 
1. Bangladesh Eight Division 
2. Division wise District 
3. All District 
4. District wise Upazilla 

To get above 4 type data, you have to set regionKey and regionsOfBanglades data jSON format properly.

Please follow below code properly.

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
		}
		,
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
	],
	"rangpurDivision": [
		{
			"parent_region_id" : "bangladesh",
			"region_name": "Panchagarh",
			"region_id": "panchagarhDistrict",
			"area": 8001,
			"population": 9794525
		},
		{
			"region_name": "Thakurgaon",
			"region_id": "thakurgaonDistrict",
			"area": 7001,
			"population": 5769750
		},
		{
			"region_name": "Dinajpur",
			"region_id": "dinajpurDistrict",
			"area": 6001,
			"population": 5557276
		},
		{
			"region_name": "Gaibandha",
			"region_id": "gaibandhaDistrict",
			"area": 5001,
			"population": 4999932
		},
		{
			"region_name": "Kurigram",
			"region_id": "kurigramDistrict",
			"area": 4001,
			"population": 4881756
		},
		{
			"region_name": "Rangpur",
			"region_id": "rangpurDistrict",
			"area": 3001,
			"population": 4377487
		},
		{
			"region_name": "Nilfamari",
			"region_id": "nilphamariDistrict",
			"area": 2001,
			"population": 4374052
		},
		{
			"region_name": "Lalmonirhat",
			"region_id": "lalmonirhatDistrict",
			"area": 1001,
			"population": 4050803
		}
	],
	"rajshahiDivision": [
		{
			"parent_region_id" : "bangladesh",
			"region_name": "Nawabganj",
			"region_id": "nawabganjDistrict",
			"area": 801,
			"population": 9794525
		},
		{
			"region_name": "Naogaon",
			"region_id": "naogaonDistrict",
			"area": 701,
			"population": 5769750
		},
		{
			"region_name": "Joypurhat",
			"region_id": "joypurhatDistrict",
			"area": 601,
			"population": 5557276
		},
		{
			"region_name": "Bogra",
			"region_id": "bograDistrict",
			"area": 501,
			"population": 4999932
		},
		{
			"region_name": "Sirajganj",
			"region_id": "sirajganjDistrict",
			"area": 401,
			"population": 4881756
		},
		{
			"region_name": "Pabna",
			"region_id": "pabnaDistrict",
			"area": 301,
			"population": 4377487
		},
		{
			"region_name": "Natore",
			"region_id": "natoreDistrict",
			"area": 201,
			"population": 4374052
		},
		{
			"region_name": "Rajshahi",
			"region_id": "rajshahiDistrict",
			"area": 101,
			"population": 4050803
		}
	],
	"barisalDivision": [
		{
			"region_name": "Barguna",
			"color_code": "#a1998;",
			"region_id": "bargunaDistrict",
			"area": 7001,
			"population" : 13434534,
			"parent_region_name": "Bangladesh",
			"parent_region_id": "bangladesh"
		},
		{
			"region_name": "Barisal",
			"color_code": "#a1998;",
			"region_id": "barisalDistrict",
			"area": 7002,
			"population" : 3434534,
		}
	],
	"rangpurDistrict": [
		{
			"parent_region_id" : "rangpurDivision",
			"region_name": "Gangachhara",
			"region_id": "gangachharaUpazila",
			"area": 5001,
			"population": 9794525
		},
		{
			"region_name": "Badarganj",
			"region_id": "badarganjUpazila",
			"area": 5001,
			"population": 5769750
		},
		{
			"region_name": "Taraganj",
			"region_id": "taraganjUpazila",
			"area": 5001,
			"population": 5557276
		},
		{
			"region_name": "Pirganj",
			"region_id": "pirganjUpazila",
			"area": 5001,
			"population": 4999932
		},
		{
			"region_name": "Mithapukur",
			"region_id": "mithapukurUpazila",
			"area": 5001,
			"population": 4881756
		},
		{
			"region_name": "Rangpur Sadar",
			"region_id": "rangpursadarUpazila",
			"area": 5001,
			"population": 4377487
		},
		{
			"region_name": "Kaunia",
			"region_id": "kauniaUpazila",
			"area": 5001,
			"population": 4374052
		},
		{
			"region_name": "Pirgachha",
			"region_id": "pirgachhaUpazila",
			"area": 5001,
			"population": 4050803
		}
	],
	"bargunaDistrict": [
		{
		  "parent_region_id": "barisalDivision",
		  "region_name": "Amtali",
		  "region_id": "amtaliUpazila",
		  "area": 43,
		  "population": 102
		},
		{
		  "region_name": "Barguna sadar",
		  "region_id": "bargunasadarUpazila",
		  "area": 43,
		  "population": 102
		},
		{
		  "region_name": "Taltali",
		  "region_id": "taltaliUpazila",
		  "area": 37,
		  "population": 101
		}
	    ]
	};	

	var selectedAllDistrict = selectedDivision = selectedDistrict = '';
	var regionKey = 'bangladesh';
	var title = 'Bangladesh MAP';

	if(selectedAllDistrict == 'allDistrict') {
		regionKey = selectedAllDistrict;
	} 

	if(selectedDivision != '') {
		regionKey = selectedDivision;
	}

	if(selectedDistrict !='') {
		regionKey = selectedDistrict;
	}

	$("#changeSvgMap").generateMap({
		'title' : title,
		'regionKey' : regionKey,
		'regionData' : regionsOfBangladesh
	});
});
</script>

```


