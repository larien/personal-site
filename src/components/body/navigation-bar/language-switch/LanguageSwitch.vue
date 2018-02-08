<template>
       <div class="container">

		<div class="switch white">

			<input type="radio" name="switch" id="switch-off">
			<input type="radio" name="switch" id="switch-on" checked>

			<label for="switch-off">BR</label>
			<label for="switch-on">EN</label>

			<span class="toggle"></span>

		</div>

	</div>
</template>


<script>
export default {

}
</script>

<style scoped>
    
body {
	background: #4a4a4a;
	color: #151515;
	font: 100%/1.5em "Lato", sans-serif;
	margin: 0;
}

input {
    font-family: inherit;
    font-size: 100%;
    line-height: normal;
    margin: 0;
}

input[type="radio"] {
    box-sizing: border-box;
    padding: 0;
}

/* ---------- SWITCH ---------- */

.container {
	height: 10%;
	left: 95%;
	position: absolute;
	top: 90%;
	width: 10%;
}

.switch {
	background: #808F9A;
	border-radius: 32px;
	display: block;
	height: 32px;
	position: relative;
	width: 80px;
}

.switch label {
	color: #fff;
	font-size: 20px;
	font-weight: 50;
	line-height: 32px;
	text-transform: uppercase;
	-webkit-transition: color .2s ease;
	-moz-transition: color .2s ease;
	-ms-transition: color .2s ease;
	-o-transition: color .2s ease;
	transition: color .2s ease;
	width: 50px;
}

.switch label:nth-of-type(1) {
	left: -75%;
	position: absolute;
	text-align: right;
}

.switch label:nth-of-type(2) {
	position: absolute;
  right: -75%;
	text-align: left;
}

.switch input {
	height: 64px;
	left: 0;
	opacity: 0;
	position: absolute;
	top: 0;
	width: 160px;
	z-index: 2;
}

.switch input:checked~label:nth-of-type(1) { color: #fff; }
.switch input:checked~label:nth-of-type(2) { color: #808F9A; }

.switch input~:checked~label:nth-of-type(1) { color: #808F9A; }
.switch input~:checked~label:nth-of-type(2) { color: #fff; }

.switch input:checked~.toggle {
	left: 5%;
}

.switch input~:checked~.toggle {
	left: 60%;
}

.switch input:checked {
	z-index: 0;
}

.toggle {
	background: #1B2836;
	border-radius: 50%;
	height: 80%;
	left: 0;
	position: absolute;
	top: 3px;
	-webkit-transition: left .2s ease;
	-moz-transition: left .2s ease;
	-ms-transition: left .2s ease;
	-o-transition: left .2s ease;
	transition: left .2s ease;
	width: 35%;
	z-index: 1;
}
</style>
    
   