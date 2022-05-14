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
