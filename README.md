# Target
Teste para estágio


/* 1. Observe o trecho de código abaixo:
   
int INDICE = 13, SOMA = 0, K = 0;
enquanto K < INDICE faça
{ K = K + 1; SOMA = SOMA + K; } imprimir(SOMA);

Ao final do processamento, qual será o valor da variável SOMA? */

let indice = 13;
let soma = 0;

for (var k = 0; k < indice; k++) {
  soma += k;
}
function newContent() {
  document.querySelector("#resultadoSoma").innerHTML = soma;
}

// O resultado da variável SOMA é: 78

/* 2. Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma
 dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na
 linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne
 uma mensagem avisando se o número informado pertence ou não a sequência.

IMPORTANTE:

Esse número pode ser informado através de qualquer entrada de sua preferência ou pode ser previamente 
definido no código;

*/

function fibonacci(n) {
  if (n <= 1) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}

const numeroVerificado = 13;
let pertence = false;

for (let i = 0; i <= numeroVerificado; i++) {
  if (fibonacci(i) === numeroVerificado) {
    pertence = true;
    break;
  }
}

if (pertence) {
  console.log(`${numeroVerificado} pertence à sequência de Fibonacci.`);
} else {
  console.log(`${numeroVerificado} não pertence à sequência de Fibonacci.`);
}



// 3. Descubra a lógica e complete o próximo elemento:
// a) 1, 3, 5, 7, \_\_\_

// Resposta: Somar 2 ao último elemento, sendo a resposta o número 9.

// b) 2, 4, 8, 16, 32, 64, \_\_\_\_
// Resposta: Multiplicar o último número por 2 ou somar o último número com ele mesmo, sendo a resposta 128 que é a soma de 64 + 64 ou 64 *2.

//c) 0, 1, 4, 9, 16, 25, 36, \_\_\_\_
// Resposta: A lógica para encontrar o próximo número é encontrar o quadrado do próximo número inteiro não negativo. Sendo assim a resposta é 49, pois 7 * 7 = 49.

// d) 4, 16, 36, 64, \_\_\_\_
// Resposta: O próximo número é 100, pois a sequência é realizada através da multiplicação do último número par por ele mesmo, onde o próximo número par dessa sequência seria o 10 e 10 * 10 = 100.

// e) 1, 1, 2, 3, 5, 8, \_\_\_\_
// Resposta: Essa é a sequência de Fibonacci. A sequência começa com os números 1 e 1. Cada número subsequente na sequência é a soma dos dois números anteriores, onde 5 + 8 = 13.

// f) 2,10, 12, 16, 17, 18, 19, \_\_\_\_
// Resposta: Não há como saber o próximo número visto que não há uma sequência lógica nesse contexto. Pra descobrir o próximo número precisaria de mais alguma informação adicional. 


// 4 - Dois veículos (um carro e um caminhão) saem respectivamente de cidades opostas pela mesma rodovia. O carro de Ribeirão Preto em direção a Franca, a uma velocidade constante de 110 km/h e o caminhão de Franca em direção a Ribeirão Preto a uma velocidade constante de 80 km/h. Quando eles se cruzarem na rodovia, qual estará mais próximo a cidade de Ribeirão Preto?
// IMPORTANTE:
// a) Considerar a distância de 100km entre a cidade de Ribeirão Preto <-> Franca.
// b) Considerar 2 pedágios como obstáculo e que o caminhão leva 5 minutos a mais para passar em cada um deles e o carro possui tag de pedágio (Sem Parar)
// c) Explique como chegou no resultado.

/* Para resolver esse problema, podemos começar desenhando um diagrama para visualizar a situação:

Ribeirão Preto ---[carro]------------------------x------------------------[caminhão]--- Franca
Onde "x" é o ponto onde os veículos se encontram. Note que a distância total entre Ribeirão Preto e Franca é de 100 km, mas o ponto "x" está localizado a uma distância "d" a partir de Ribeirão Preto.

Podemos usar a fórmula:
distância = velocidade x tempo
para determinar o tempo que leva para cada veículo chegar ao ponto "x". Como a velocidade é constante para ambos os veículos, podemos simplificar para:
tempo = distância / velocidade
Para o carro:
tempo_carro = d / 110
Para o caminhão:
tempo_caminhão = (100 - d) / 80 + 2 * 5 / 60
Onde 2 * 5 / 60 é o tempo adicional que o caminhão leva para passar em dois pedágios.
Como os veículos se encontram no ponto "x", podemos igualar os tempos:
d / 110 = (100 - d) / 80 + 2 * 5 / 60
Simplificando e resolvendo para "d", obtemos:
d = 41,67 km
Portanto, o ponto "x" está a 41,67 km de Ribeirão Preto e 58,33 km de Franca.
Como resultado, podemos concluir que o caminhão estará mais próximo de Ribeirão Preto, já que ele está a uma distância de apenas 41,67 km, enquanto o carro está a uma distância de 58,33 km.
*/

// 5. Escreva um programa que inverta os caracteres de um string.
IMPORTANTE:
a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;
b) Evite usar funções prontas, como, por exemplo, reverse;

let str = "Teste 1, 2";
let invertedStr = ""; 

for (let i = str.length - 1; i >= 0; i--) {
  invertedStr += str[i];
}

console.log(invertedStr);

/* NÃO SE ESQUEÇA DE INSERIR O LINK DO SEU REPOSITÓRIO NO GITHUB COM O CÓDIGO FONTE QUE VOCÊ DESENVOLVEU .
Resposta obrigatória
