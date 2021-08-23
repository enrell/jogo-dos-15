
<style>
	@charset "UTF-8";
			.container {
			box-sizing: border-box;
			box-sizing: 0;
			width: 100%;
			height: 100%;
			margin: 0%;
			padding: 0%;
			
			font: normal 30px Arial, Helvetica, sans-serif;
		
			background-color: #170126;
		}
		:global(body) {
			margin: 0;
			padding: 0;

			background-color: #170126;
		}
		.back {
			display: inline-block;
			grid-area: footer;
			position: fixed;
			width: 15%;
			margin: 0.5vh;
			left: 80%;
			top: 90%;
			padding: 0%;
			border: none;
			outline: none;
		
			text-decoration: none;
			font: normal bolder 40px Arial, Helvetica, sans-serif;
			cursor: pointer;
		
			transition: all 1s;
			transition-duration: 0.4s;
			
			background-color: #270140;
			box-shadow: 0 10px #170126;
			color: #44D2F2;
			
		}

		/*----Container da pagina----*/
		
		.game {
			display: grid;
			grid-template-columns: 0.5fr 1fr 0.5fr;
			grid-template-rows: 0.5fr 1fr 0.1fr;
			grid-auto-columns: 1fr;
			grid-auto-rows: 1fr;
			gap: 0px 0px;
			width: 100%;
			height: 100%;
			grid-auto-flow: row;
			align-items: stretch;
			grid-template-areas:
				"header header header"
				"difficulty gamearea time"
				"footer footer footer";
		}
		
		/*----Header----*/
		
		.header {
			grid-area: titulo;
			text-align: center;
			margin: 0%;

			font: normal bolder 4em Arial;

			color: #44D2F2;
			background-color: #170126;
		}
		/*----area dos blocos----*/
		.gamearea {
			position: relative;
			margin: 0 auto;
			padding: 2px;
			width: 400px;
			height: 400px;
			
			background: #170126;
			box-shadow: 0 0 4px 4px #44D2F2;
			
		
		}
		
		/*----Animacao dos blocos----*/
		
		.gamearea .item.item-1{
			transform: translate(0px, 0px);
		}
		.gamearea .item.item-2{
			transform: translate(100px, 0px);
		}
		.gamearea .item.item-3{
			transform: translate(200px, 0px);
		}
		.gamearea .item.item-4{
			transform: translate(300px, 0px);
		}
		.gamearea .item.item-5{
			transform: translate(0px, 100px);
		}
		.gamearea .item.item-6{
			transform: translate(100px, 100px);
		}
		.gamearea .item.item-7{
			transform: translate(200px, 100px);
		}
		.gamearea .item.item-8{
			transform: translate(300px, 100px);
		}
		.gamearea .item.item-9{
			transform: translate(0px , 200px);
		}
		.gamearea .item.item-10{
			transform: translate(100px, 200px);
		}
		.gamearea .item.item-11{
			transform: translate(200px, 200px);
		}
		.gamearea .item.item-12{
			transform: translate(300px, 200px);
		}
		.gamearea .item.item-13{
			transform: translate(0px, 300px);
		}
		.gamearea .item.item-14{
			transform: translate(100px, 300px);
		}
		.gamearea .item.item-15{
			transform: translate(200px, 300px);
		}
		.gamearea .item.item-16{
			transform: translate(300px, 300px);
		}
		
		
		.gamearea .item {
			position: absolute;
			top: 0;
			left: 0;
			width: 25%;
			height: auto;
			text-align: center;
			margin: 0;
			padding: 0;
			border: none;
			
			cursor: pointer;
			transition: transform .3s ease-out;
			
			color: black;
		}
		*, :after, :before {
			box-sizing: border-box;
		}
		
		.gamearea .item-label {
				height: 25%;
				padding: 16px;
				margin: 0px;
				line-height: 2;

				font-size: 35px;
				font-weight: 300;

				background: #7107b8;
				box-shadow: inset 0 0 0 3px #170126;
		
		}
		*, :after, :before {
			box-sizing: border-box;
		}
		
		
		.difficulty{
			grid-area: difficulty;
			position: relative;
			width: 100%;
			height: 100%;
			margin: 2vh;
			left: 1%;

			color: #44D2F2;
			background-color: #270140;
		}
		.difficulty, h2 {
			text-align: center;
		}
		
		.button {
			position: relative;
			text-align: center;
			align-items: center;
			top: -20px;
			width: 50%;
			height: 12%;
			margin: 2vh;
			border: none;
			
			text-decoration: none;
			font: normal bolder 20px Arial, Helvetica, sans-serif;
			cursor: pointer;
			
			transition: all 1s;
			transition-duration: 0.4s;
				
			background-color: #270140;
			color: #44D2F2;
			box-shadow: 0 10px #170126;
		}
		
		.button span {
			cursor: pointer;
			display: inline-block;
			position: relative;
			transition: 0.6s;
		}
		.button:hover {
			background-color: #10001b;
		}
		.button:active {
			background-color: #10001b;
			box-shadow: 0 5px #10001b;
			transform: translateY(5px);
		}
		
		.footer { 
			grid-area: footer;
			width: 100%;
			
		}
		
		.header { 
			grid-area: header;
			width: 100%;
			height: 100%;
		}
		
		.time { 
			grid-area: time;
			width: 100%;
			height: 100%;
		}
</style>
	
<script>

	var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16]
function item1(){
	const backup16 = array[15]
	if (array[0] < array[15]){
		array[15] = array[0]
		array[0] = backup16
		
	}
else{
	array[15] = array[4]
	array[0] = backup16
}
}
function item2(){
	const backup16 = array[15]
	if (array[1] < array[15]){
		array[15] = array[1]
		array[1] = backup16
		
	}
else{
	array[15] = array[1]
	array[1] = backup16
}
}
function item3(){
	const backup16 = array[15]
	if (array[2] < array[15]){
		array[15] = array[2]
		array[2] = backup16
		
	}
else{
	array[15] = array[2]
	array[2] = backup16
}
}
function item4(){
	const backup16 = array[15]
	if (array[3] < array[15]){
		array[15] = array[3]
		array[3] = backup16
		
	}
else{
	array[15] = array[3]
	array[3] = backup16
}
}
function item5(){
	const backup16 = array[15]
	if (array[4] < array[15]){
		array[15] = array[4]
		array[4] = backup16
		
	}
else{
	array[15] = array[4]
	array[4] = backup16
}
}
function item6(){
	const backup16 = array[15]
	if (array[5] < array[15]){
		array[15] = array[5]
		array[5] = backup16
		
	}
else{
	array[15] = array[5]
	array[5] = backup16
}
}
function item7(){
	const backup16 = array[15]
	if (array[6] < array[15]){
		array[15] = array[6]
		array[6] = backup16
		
	}
else{
	array[15] = array[6]
	array[6] = backup16
}
}
function item8(){
	const backup16 = array[15]
	if (array[7] < array[15]){
		array[15] = array[7]
		array[7] = backup16
		
	}
else{
	array[15] = array[7]
	array[7] = backup16
}
}
function item9(){
	const backup16 = array[15]
	if (array[8] < array[15]){
		array[15] = array[8]
		array[8] = backup16
		
	}
else{
	array[15] = array[8]
	array[8] = backup16
}
}
function item10(){
	const backup16 = array[15]
	if (array[9] < array[15]){
		array[15] = array[9]
		array[9] = backup16
		
	}
else{
	array[15] = array[9]
	array[9] = backup16
}
}
function item11(){
	const backup16 = array[15]
	if (array[10] < array[15]){
		array[15] = array[10]
		array[10] = backup16
		
	}
else{
	array[15] = array[10]
	array[10] = backup16
}
}
function item12(){
	const backup16 = array[15]
	if (array[11] < array[15]){
		array[15] = array[11]
		array[11] = backup16
		
	}
else{
	array[15] = array[11]
	array[11] = backup16
}
}
function item13(){
	const backup16 = array[15]
	if (array[12] < array[15]){
		array[15] = array[12]
		array[12] = backup16
		
	}
else{
	array[15] = array[12]
	array[12] = backup16
}
}
function item14(){

		const backup16 = array[15]
	if (array[13] < array[15]){
		array[15] = array[13]
		array[13] = backup16
		
	}
else{
	array[15] = array[13]
	array[13] = backup16
}
}

	

function item15(){
	const backup16 = array[15]
	if (array[14] < array[15]){
		array[15] = array[14]
		array[14] = backup16
		
	}
else{
	array[15] = array[14]
	array[14] = backup16
}
}
function reset(){
	array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16]
}
function easy(){
	array = [1, 2, 4, 8, 9, 5, 3, 12, 13, 6, 7, 15, 10, 14, 11, 16]
}
function normal(){
	array = [9, 10, 3, 2, 1, 6, 7, 8, 4, 11, 5, 12, 13, 14, 15]
}
function hard(){
	array = [11, 10, 15, 12, 13, 3, 8, 4, 9, 5, 1, 2, 14, 7, 6]
}
	
</script>
<svelte:head>
	<link rel="shortcut icon" href="./favicon.ico" type="image/vnd.microsoft.icon">
	<title>GAME</title>
</svelte:head>
<div class="container">

		<div class="game">
			<div class="gamearea">
			
				<button class="item item-{array[0]} label-1" on:click="{item1}"><div class="item-label">1</div></button>
				<button class="item item-{array[1]} label-2" on:click="{item2}"><div class="item-label">2</div></button>
				<button class="item item-{array[2]} label-3" on:click="{item3}"><div class="item-label">3</div></button>
				<button class="item item-{array[3]} label-4" on:click="{item4}"><div class="item-label">4</div></button>
				<button class="item item-{array[4]} label-5" on:click="{item5}"><div class="item-label">5</div></button>
				<button class="item item-{array[5]} label-6" on:click="{item6}"><div class="item-label">6</div></button>
				<button class="item item-{array[6]} label-7" on:click="{item7}"><div class="item-label">7</div></button>
				<button class="item item-{array[7]} label-8" on:click="{item8}"><div class="item-label">8</div></button>
				<button class="item item-{array[8]} label-9" on:click="{item9}"><div class="item-label">9</div></button>
				<button class="item item-{array[9]} label-10" on:click="{item10}"><div class="item-label">10</div></button>
				<button class="item item-{array[10]} label-11" on:click="{item11}"><div class="item-label">11</div></button>
				<button class="item item-{array[11]} label-12" on:click="{item12}"><div class="item-label">12</div></button>
				<button class="item item-{array[12]} label-13" on:click="{item13}"><div class="item-label">13</div></button>
				<button class="item item-{array[13]} label-14" on:click="{item14}"><div class="item-label">14</div></button>
				<button class="item item-{array[14]} label-15" on:click="{item15}"><div class="item-label">15</div></button>
				<button class="item item-{array[15]} label-16"></button>
			</div>
		
					<div class="difficulty">
						<h2>Select difficulty</h2>
						<button class="button" on:click="{reset}"><span>Reset</span></button>
						<button class="button" on:click="{easy}"><span>Easy</span></button>
						<button class="button" on:click="{normal}"><span>Normal</span></button>
						<button class="button" on:click="{hard}"><span>Hard</span></button>
						</div>
					<div class="footer"></div>
					<div class="header">GAME OF FIFTEEN</div>
					<div class="time"></div>
				</div>

</div>
