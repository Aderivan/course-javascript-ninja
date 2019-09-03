# Desafio da semana #5

```js
/*
Crie uma variável qualquer, que receba um array com alguns valores aleatórios
- ao menos 5 - (fica por sua conta os valores do array).
*/
 var myArray = ['josé', 29, 'Andreza', 25, 'brother'];


/*
Crie uma função que receba um array como parâmetro, e retorne esse array.
*/
function myFunction (arg) {
    return arg;
}

/*
Imprima o segundo índice do array retornado pela função criada acima.
*/
 console.log(myFunction(myArray)[2])

/*
Crie uma função que receba dois parâmetros: o primeiro, um array de valores; e o
segundo, um número. A função deve retornar o valor de um índice do array que foi passado
no primeiro parâmetro. O índice usado para retornar o valor, deve ser o número passado no
segundo parâmetro.
*/
var myArray = ['josé', 29, 'Andreza', 25, 'brother'];

function myFunction (arg, indice) {
    return !indice ? arg : arg[indice];
}

console.log(myFunction(myArray, 1))


/*
Declare uma variável que recebe um array com 5 valores, de tipos diferentes.
*/
 var myArray = ['josé', 29, true, 'araújo', 'sagitário'];

/*
Invoque a função criada acima, fazendo-a retornar todos os valores do último
array criado.
*/
function myFunction () {
    return myArray;
}

/*
Crie uma função chamada `book`, que recebe um parâmetro, que será o nome do
livro. Dentro dessa função, declare uma variável que recebe um objeto com as
seguintes características:
- esse objeto irá receber 3 propriedades, que serão nomes de livros;
- cada uma dessas propriedades será um novo objeto, que terá outras 3
propriedades:
    - `quantidadePaginas` - Number (quantidade de páginas)
    - `autor` - String
    - `editora` - String
- A função deve retornar o objeto referente ao livro passado por parâmetro.
- Se o parâmetro não for passado, a função deve retornar o objeto com todos
os livros.
*/

function book(bookName) {
    var allBooks = {
        'alto da compadecida': {
            quantidadeDePaginas: 200,
            autor: 'Ariano Suassuna',
            editora: 'saraiva'
        },
        'dom casmurro': {
            quantidadeDePaginas: 300,
            autor: 'Machado de Assis',
            editora: 'Viseu'
        },
        'Rosa dos ventos': {
            quantidadeDePaginas: 100,
            autor: 'Bartolomeu',
            editora: 'global'
        }
    }

    return !bookName ? allBooks : allBooks[bookName];
}
console.log(book('Rosa dos ventos'));

/*
Usando a função criada acima, imprima o objeto com todos os livros.
*/
 console.log(book());

/*
Ainda com a função acima, imprima a quantidade de páginas de um livro qualquer,
usando a frase:
"O livro [NOME_DO_LIVRO] tem [X] páginas!"
*/
 console.log('O livro Rosa dos ventos tem ' + book('Rosa dos ventos').quantidadeDePaginas + ' páginas');

/*
Ainda com a função acima, imprima o nome do autor de um livro qualquer, usando
a frase:
"O autor do livro [NOME_DO_LIVRO] é [AUTOR]."
*/
 var bookName = 'dom casmurro';
console.log('O autor do livro ' + bookName + ' é ' + book(bookName).autor);

/*
Ainda com a função acima, imprima o nome da editora de um livro qualquer, usando
a frase:
"O livro [NOME_DO_LIVRO] foi publicado pela editora [NOME_DA_EDITORA]."
*/
var bookName = 'dom casmurro';
console.log('O livro ' + bookName + ' foi publicado pela editora ' + book(bookName).editora);
