# Desafio da semana #9
```js

(function () {


/*
Crie uma IIFE que envolva todo o código desse arquivo. Faça também a
indentação correta do código, para ficar dentro da IIFE.
*/ 
/*
Analise as funções abaixo (`myFunction`, `myFunction2` e `myFunction3`, e
ajuste o posicionamento das variáveis e funções internas, para que os códigos
dentro de `console.log` que estão retornando `undefined` retornem o valor
correto da variável ou função chamada.
*/
/*
Analise as funções abaixo (`myFunction`, `myFunction2` e `myFunction3`, e
ajuste o posicionamento das variáveis e funções internas, para que os códigos
dentro de `console.log` que estão retornando `undefined` retornem o valor
correto da variável ou função chamada.
*/
function myFunction() {
    var number1 = 10;
    var number2 = 20;
    console.log('============ myFunction ============ ')
    console.log('Na função `myFunction`, o primeiro número é', number1);
    console.log('Na função `myFunction`, o segundo número é', number2);
    return number1 + number2;
}
myFunction();

/*
    myFunction2();
*/
function myFunction2() {
    var number1 = 10;
    var number2 = 20;
    var sum = function sum() {
        return number1 + number2;
    };
    console.log()
    console.log('============ myFunction2 ============ ')
    console.log('A soma de 10 e 20 é igual a', sum ? sum() : undefined);
    return sum();
}
myFunction2();

/*
    myFunction3();
*/
function myFunction3() {
    console.log()
    console.log('============ myFunction2 ============ ')
    var number1 = 40;
    var number2 = 50;
    function sum() {
        console.log('Na função myFunction3, number1 é igual a', number1);
        return number1 + number2;
    }
    console.log('A soma de 40 e 50 é igual a', sum());
    return sum();
};
myFunction3();

/*
No desafio anterior criamos uma calculadora, usando uma estrutura funcional.
Agora vamos criar uma outra calculadora, usando uma outra abordagem :D
- Crie uma função `calculator` que recebe dois valores (números)
por parâmetro.
- Essa função deve retornar uma outra função, que recebe um parâmetro
chamado `callback`.
- Esse `callback` será uma função, que passaremos por parâmetro ao invocar
o retorno de `calculator`.
- O retorno dessa segunda função deve ser a função de `callback` passada
por parâmetro, INVOCADA, e passando a ela por parâmetro os dois valores
que foram passadas para a primeira função `calculator`.
*/

function calculator(number1,number2) {
    return function(callback) {
        return callback(number1, number2);
    }; 
}

/*
Declare uma variável chamada `sum`, e atribua a ela a função `calculator`,
passando dois números por parâmetro.
*/

var sum = calculator(3,5);

/*
Sabemos que `sum` agora tem uma função atribuída a ela, que é o retorno de
`calculator`. E essa função espera um parâmetro `callback`. O `callback`
tem dois parãmetros disponíveis, que são os números que você acabou de passar
para a chamada à `calculator` acima.
- Mostre no console o retorno da invocação de `sum`, passando por parâmetro
uma função anônima que irá retornar a soma dos dois números que essa função
anônima tem como seus argumentos.
*/
console.log( 'O resultado da soma é:' );
// ?

/*
Agora declare outra variáveis chamadas `subtraction`, `multiplication`,
`division` e `mod`, e atribua à elas `calculator`, passando números
diferentes para cada chamada.
*/
// ?

/*
Mostre as variáveis acima no `console` (uma chamada de console por variável),
criando a função de `callback` que faz o cálculo para subração, multiplicação,
divisão e módulo (resto de divisão), conforme a função utilizada.
As suas respostas devem estar abaixo dos `console.log` referentes à cada
chamada.
*/
subtracao = calculater(6,2);
console.log('O resultado da subtração é: ', subtracao(function(number1, number2) {
    return number1 - number2;
}))

multiplicacao = calculater(6,2);
console.log('O resultado da subtração é: ', multiplicacao(function(number1, number2) {
    return number1 * number2;
}))

divisao = calculater(6,2);
console.log('O resultado da subtração é: ', divisao(function(number1, number2) {
    return number1 / number2;

resto = calculater(4,2);

console.log('O resultado da soma é: ', resto(function(number1, number2) {
    return number1 % number2;
}));
}))
})();