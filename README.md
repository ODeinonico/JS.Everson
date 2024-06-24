# JS.Everson
Código html
//variáveis da bolinha let xBolinha = 100; let yBolinha = 200; let diametro = 19; let raio diametro / 2;

//velocidade da bolinha let velocidadeXBolinha = 6; let velocidadeYBolinha = 6;

//variáveis da raquete let xRaquete = 5; let yRaquete = 150; let raqueteComprimento = 10; let raqueteAltura = 90;

//variáveis do oponente let xRaqueteOponente = 585; let yRaqueteOponente = 150; let velocidade YOponente;

let colidiu = false;

//placar do jogo let meusPontos = 0; let pontosDoOponente = 0;

//sons do jogo let raquetada;

let ponto;

let trilha;

function preload(){ trilha ponto loadSound("trilha.mp3"); loadSound("ponto.mp3"); raquetada loadSound("raquetada.mp3"); }

function setup() {
createCanvas(600, 400); trilha.loop();

}
function draw() {

background(0);

mostraBolinha();

movimentaBolinha();

verificaColisaoBorda();

mostraRaquete (xRaquete, yRaquete);

movimentaMinhaRaquete();

//verificaColisaoRaquete();

verificaColisaoRaquete (xRaquete, yRaquete);

mostraRaquete (xRaqueteOponente, yRaqueteOponente);

movimentaRaqueteOponente();

verificaColisaoRaquete (xRaqueteOponente,

yRaqueteOponente);

incluiPlacar();

marcarPonto();

}

function mostraBolinha() {

circle(xBolinha, yBolinha, diametro);

}

function movimentaBolinha() {

xBolinha + velocidadeXBolinha;

yBolinha += velocidadeYBolinha;

}

function verificaColisaoBorda() {

if (xBolinha + raio > width || xBolinha -

raio < 0) {

velocidadeXBolinha = -1;

} if (yBolinha + raio > height || yBolinha

raio < 0) {

velocidadeYBolinha *= -1;

}

}

function mostraRaquete (x,y) {

rect(x, y, raqueteComprimento, raqueteAltura);

}

if (keyIsDown(UP_ARROW)) {

function movimentaMinhaRaquete() {

yRaquete 10;

}

if (keyIsDown(DOWN_ARROW)) {

yRaquete += 10;

}

}
