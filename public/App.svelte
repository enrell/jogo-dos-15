<script>

</script>

<svelte:head>
	<link rel="stylesheet" href="./global.css">
	<link rel="shortcut icon" href="./favicon.ico" type="image/vnd.microsoft.icon">
	<title>Menu</title>
</svelte:head>

<div class="container">
	<div class="titulo">GAME OF FIFTEEN</div>

		<button class="button-1" onclick="window.location.href='./game.svelte'"><span>PLAY</span></button>
		<button class="button-2" onclick="window.location.href='./sobre.html'"><span>ABOUT</span></button>

<div class="footer"></div>
		
	<div class="none-01"></div>
	<div class="none-02"></div>
	<div class="none-03"></div>
	<div class="none-04"></div>
</div>

<style>

@charset "UTF-8";
@import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');

.container {
text-align: center;
display: grid;
width: 100%;
right: 100%;
margin: 0;
padding: 0;
box-sizing: border-box;
background-color: #270140;
grid-template-columns: 1fr 1fr 1fr;
grid-template-rows: 1fr 1fr 1fr;
grid-template-areas: 
	"titulo titulo titulo"
	"none-01 button-1 none-02"
	"none-03 button-2 none-04"
	"footer footer footer";
	font: normal bolder 30px Arial, Helvetica, sans-serif;
	
}
.titulo {
grid-area: titulo;
color: #44D2F2;
background-color: #170126;
font: normal bolder 4em Arial;
text-align: center;
margin: 0%;
}
.button-1 {
font: normal bolder 30px Arial, Helvetica, sans-serif;
grid-area: button-1;
background-color: #270140;
border: none;
color: #44D2F2;
padding: 0;
width: 100%;
right: 100%;
text-decoration: none;
display: inline-block;
margin: 10px;
cursor: pointer;
transition: all 1s;
transition-duration: 0.4s;
outline: none;
box-shadow: 0 10px #170126;
}
/* Define, quando meu cursor estiver acima do bot�o ele vai ativar a anima��o */
.button-1 span {
cursor: pointer;
display: inline-block;
position: relative;
transition: 0.6s;
}
.button-1 span:after {
content: "<<";
position: absolute;
opacity: 0;
top: 0;
right: -50px;
transition: 0.6s;
}
.button-1:hover span {
padding-right: 50px;
}
.button-1:hover span:after {
opacity: 1;
right: 0;
}
.button-1:hover {
background-color: #10001b;
}
.button-1:active {
background-color: #10001b;
box-shadow: 0 5px #10001b;
transform: translateY(5px);
}

.button-2 {
font: normal bolder 30px Arial, Helvetica, sans-serif;
grid-area: button-2;
background-color: #270140;
border: none;
color: #44D2F2;
padding: 0%;
width: 100%;
right: 100%;
text-align: center;
text-decoration: none;
display: inline-block;
margin: 1%;
cursor: pointer;
transition: all 1s;
transition-duration: 0.4s;
outline: none;
box-shadow: 0 10px #170126;

}
.button-2 span {
cursor: pointer;
display: inline-block;
position: relative;
transition: 0.6s;
}
.button-2 span:after {
content: "<<";
position: absolute;
opacity: 0;
top: 0;
right: -50px;
transition: 0.6s;
}
.button-2:hover span {
padding-right: 50px;
}
.button-2:hover span:after {
opacity: 1;
right: 0;
}
.button-2:hover {
background-color: #10001b;
}
.button-2:active {
background-color: #10001b;
box-shadow: 0 5px #10001b;
transform: translateY(4px);
}
.none-01 {
grid-area: none-01;
}
.none-02 {
grid-area: none-02;
}
.none-03 {
grid-area: none-03;
}
.none-04 {
grid-area: none-04 ;
}

.footer {
grid-area: footer;
}

</style>