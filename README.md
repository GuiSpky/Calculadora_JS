# Calculadora_JS
Codigo de calculadora utilizando JS HTML e CSS
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Calculadora</title>
	<link rel="stylesheet" type="text/css" href="style.css">
	<script type="text/javascript" src="script.js"></script>	
</head>
<body>

	<div class="fundo">
		<div class="calculadora">
			<h1>Calculadora</h1>
			<div class="resultado">
			<p id="resultado"></p>
			</div>
			<table>
				<tr>
					<td><button class="botão_top" onclick="limpar()">C</button></td>
					<td><button class="botão_top" onclick="apagar()"><</button></td>
					<td><button class="botão_top" onclick="porcentagem()">%</button></td>
					<td><button class="botão_side"  onclick="insert('/')">/</button></td>
				</tr>
				<tr>
					<td><button class="botão" onclick="insert('7')">7</button></td>
					<td><button class="botão" onclick="insert('8')">8</button></td>
					<td><button class="botão" onclick="insert('9')">9</button></td>
					<td><button class="botão_side" onclick="insert('*')">X</button></td>
				</tr>
				<tr>
					<td><button class="botão" onclick="insert('4')">4</button></td>
					<td><button class="botão"onclick="insert('5')" >5</button></td>
					<td><button class="botão" onclick="insert('6')">6</button></td>
					<td><button class="botão_side" onclick="insert('-')">-</button></td>
				</tr>
				<tr>
					<td><button class="botão" onclick="insert('1')">1</button></td>
					<td><button class="botão" onclick="insert('2')">2</button></td>
					<td><button class="botão" onclick="insert('3')">3</button></td>
					<td><button class="botão_side" onclick="insert('+')">+</button></td>
				</tr>
				<tr>
					<td colspan="2"><button class="botão_zero" onclick="insert('0')">0</button></td>
					<td><button class="botão" onclick="insert('.')">.</button></td>
					
					<td><button class="botão_side" onclick="calcular()">=</button></td>
				</tr>
			</table>
		</div>	
	</div>

</body>
</html>

//css

*{margin: 0; padding: 0;}
.fundo{background-color: #f2f2f2;
	height: 100vw;
font-family: arial;}
.calculadora{
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%,-50%);
	background-color: black;
	padding: 15px;
	border-radius: 25px;
}
p,h1{color: white;}
.botão,.botão_top,.botão_side{
	height: 50px;
	width: 50px;
	font-size: 25px;
	cursor: pointer;
	border-radius: 50px;
	border-style: none;
	margin: 1px;
}
.botão_zero{
	height: 50px;
	width: 100px;
	font-size: 25px;
	cursor: pointer;
	border-radius: 50px;
	border-style: none;	
	margin: 1px;
}
.botão,.botão_zero{
	background-color: #353535;
	color: #ffffff;
}
.botão:hover,.botão_zero:hover{
	background-color: #808080;
}
.botão_side{
	background-color: #d16704;
	color: #ffffff;
}
.botão_side:hover{
	background-color: #c78a52;
}
.botão_top{
	background-color: #808080;
}
.botão_top:hover{
	background-color: #dddddd;
}
#resultado{
	width: 207px;
	height: 50px;
	font-size: 40px;
	color: #FFFFFF;
	text-align: right;
	padding: 5px;
}
.resultado{
	overflow: auto;
}

//JavaScript


function insert(num) {
	
	var numero = document.getElementById('resultado').innerHTML;
	document.getElementById('resultado').innerHTML = numero + num;
}
function limpar( ) {
	document.getElementById('resultado').innerHTML = " ";
}
function apagar( ) {
	var resultado = document.getElementById('resultado').innerHTML;
	document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length - 1);
}
function calcular( ) {
	var resultado = document.getElementById('resultado').innerHTML;
	if (resultado) {
		document.getElementById('resultado').innerHTML = eval(resultado);
	}
}
function porcentagem(){
	var resultado = document.getElementById('resultado').innerHTML;
	document.getElementById('resultado').innerHTML = (resultado/100) 
}
