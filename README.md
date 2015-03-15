```
<meta charset="UTF-8">
<canvas id="tela" width="600" height="400"></canvas>

<script>

var tela = document.getElementById("tela");
var c = tela.getContext("2d");

var circuloAzul = function(x,y,raio) {
	c.fillStyle = "blue";
	c.beginPath();
	c.arc(x,y,raio, 0, 2 * Math.PI);
	c.fill();
}
var circuloVermelho = function(x,y,raio) {
	c.fillStyle = "red";
	c.beginPath();
	c.arc(x,y,raio, 0, 2 * Math.PI);
	c.fill();
}

var limpaTela = function(){
	c.clearRect(0, 0, 600, 400);
}

var x = 1;
var x1 = 600;
var y = 400;

var desenha = function() {
	limpaTela();
	circuloVermelho(x, 100, 10);
	circuloVermelho(400, y, 10);
	circuloAzul(x1, 200,10);
	circuloAzul(200, x, 10);
	x = x + 1;
	x1 = x1 - 1;
	y = y - 1;
}

setInterval(desenha, 30);

</script>
```
