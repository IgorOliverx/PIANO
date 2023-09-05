# PIANO JavaScript

O piano, dado inicialmente na dificuldade fácil, é um 'projeto simples" que estimula a lógica de programação e introduz conceitos básicos da linguagem JavaScript de uma forma interativa e que ainda lhe permite desbravar eventos, funções e manipulação de variáveis. Apesar de "simples" é um ótimo programa para se testar.


EXPLICANDO O CÓDIGO:

Inicialmente temos a criação de alguns botões e tags do tipo audio. Cada botão teve um id único designado para poder ser manipulado no js e que permitiu a interação. 
"<button id="btn1"></button>"
"<audio id="audio" src="sons/do8.wav"></audio>"
Baixei as 8 notas musicais numa plataforma de aúdios online no formato .wav e os aloquei na pastas sons.
Posteriormente comecei a manipular os id dentro do código js, observe:

"const btn = document.getElementById('btn');
btn.addEventListener('click', function () {
    const audio = document.getElementById('audio');
    audio.play();
})"

Primeiro criei uma constante chamada btn que serviu para eu alocar o id 'btn' presente no código html e em seguinte, adicionei um evento à constante com o ouvinte 'click' que executa uma ação postergada.
Repare que o evento 'click' desencadeia a reação que foi criada dentro da function(
    Uma constante para alocar o audio do html dentro do js, entao eu pego seu id e manipulo-o e após tê-lo no js, uso uma função simples que é a .play() que no caso, startou o aúdio após acontecer o click.
); 

OBS:Após alguns testes, consegui manipular de forma que o main.js ficasse curto e eficaz, iterei em um laço que corre os botoes de 0 a 30: desta forma:

for (let i = 0; i <= 30; i++) {
    const btn = document.getElementById(`btn${i}`);
    const audio = document.getElementById(`audio${i}`);
    btn.addEventListener('click', function () {
        audio.play();
    });
}


 OUTRO JEITO DE FAZER É POR MEIO DE FUNÇÕES - TESTEI ESSE INICIALMENTE COM ITERAÇÃO MAS NAO CONSEGUI O EXECUTAR CADA UM COM UM SOM - LEMBRE-SE DE COLOCAR A FUNCTION NA CLASSE DO BOTAO COM O ONCLICK(no html) 
 function som() {
     btn.addEventListener('click', function() {
         const audio = document.getElementById('audio')
        audio.play();
   } )
}


Criei também uma function que mostrava uma onda sonora embaixo da tecla quando clicado, essa funciona muito bem, o real problema é encontrar um bom video e ainda por cima sem o fundo
function mostrarOnda () {
    const vid = document.getElementById('vid');
    vid.style.display = "block";
    //função para fazer ondas sonoras aparecerem - ela funciona, mas nao consigo um video bom :)
}


