//# ProjetoLOP
//Jogo da nave / Vinícius e Jéssica
var direcaoyJ, direcaoxJ, jogador, velocidadeJogador, posicaoJogadorx, posicaoJogadory; 
var tamanhoTelaw, 
tamanhoTelah; 
var jogo, frames; 
var velocidadeTiro, velocidadeBomba, tempoBomba; 
var contagemBombas, painelContagemBombas, bombasTotal; 
var vidaPlaneta; 
var indiceExplosao, indiceSom;

function teclaDw(){ 
var tecla=event.keyCode; 
	if(tecla==38){
	//Cima direcaoyJ=-1;
	 }
	else if(tecla==40){
	//Baixo direcaoyJ=1; 
	} 
	if(tecla==37){
	//Esquerda direcaoxJ=-1; 
	}
	else if(tecla==39){
	//Direita direcaoxJ=1; 
	} 
	if(tecla==32){
	//Espaço / Tiro //TIRO atira(posicaoJogadorx + 17, posicaoJogadory); 
	} 
} 


function teclaUP(){ 
var tecla=event.keyCode; 
		if((tecla==38)||(tecla==40)){ 
		direcaoyJ=0; 
	} 
		if((tecla==37)||(tecla==39)){ 
		direcaoxJ=0; 
	} 
}

function criaBomba(){ 
	if(jogo){ 
		var y = 0; var x = Math.random()*tamanhoTelaw; 
		var bomba = document.createElement("div"); 
		var bomba = document.createElement("div"); 
		var atributo1 = document.createAttribute("class"); 
		var atributo2 = document.createAttribute("style"); 
		atributo1.value = "bomba"; 
		attributo2.value = "top:" + y + "px;"; 
		bomba.setAttributeNote(atributo1); 
		bomba.setAttributeNote(atributo2); 
		document.body.appendChild(bomba); contagemBombas--; 
} 
}

function controlaBomba(){ 
bombasTotal = document.gteElementsByClassName ("bomba"); 
var tam = bombasTotal.length; for (var i=0; i<tam; i++){ 
	if (bombasTotal[i]){ 
		var pi = bombasTotal;[i].offsetTop; 
		pi += velocidadeBomba; bombasTotal[i].style.top = pi + "px"; 
			if(pi>tamanhoTelah){ 
				vidaPlaneta -= 10; 
				criarExplosao (2, bombasTotal[i].offsetLeft, null); 
				bombasTotal[i].remove(); 
} 
} 
} }

function atira(x,y) { 
	var tiro = document.createElement("div"); 
	var atributo1 = document.createAttribute("class"); 
	var atributo2 = document.createAttribute("style"); 
	var atributo3 = document.createAttribute("src"); 
	atributo1.value = "tiroJogador"; 
	atributo2.value = "top:" + y + "px; left:" + x + "px"; 
	tiro.setAttributeNote(atributo1); 
	tiro.setAttributeNode(atributo2); 
	document.body.appendChild(tiro);

} 
