Dia :: 2025-05-25
### Anotação rápida
- Ele recebe uma função de callback que irá iterar sobre cada um dos elementos do meu array. 
- Não modifica o array que filtrou, então tem que criar um outro array para receber o que ele filtrou
- Ele automaticamente passa 3 argumentos para a função de callback -> `function callbackFilter(valor, índice, array) {}`
	- `valor` -> É o valor mesmo que ta no array, por exemplo 5.
	- `índice` -> o índice desse valor, nesse caso 0.
	- `array` -> retorna o array inteiro.
- Ele funciona como um `for of` -> Passa pelo valor no índice 0, executa a função callback, depois pelo valor no índice 1, executa a funçã callback até o fim.
- O método `.filter()`, requer que a função callback retorne um valor booleano -> `true`( Para quando você quiser que aquele valor seja imbutido no novo array ) or `false` ( Para quando você quiser que aquele valor não seja imbutido no novo array ); 

```js
// Retorne os números maiores que 10  
const numbers = [5, 50, 80, 1, 2, 3, 5, 8, 7, 11, 15, 22, 27];
const numbersFiltered = numbers.filter((valor) => {
	return valor > 10
});
```
> Acima temos um filtro com uma arrow function que receber um argumento com o valor do array e retorna `true` or `false` ao verificar se o argumento recebido é maior que 10.

```js
// Retorne os números maiores que 10  
const numbers = [5, 50, 80, 1, 2, 3, 5, 8, 7, 11, 15, 22, 27];
const numbersFiltered = numbers.filter(valor => return valor > 10);
```
> Acima temos a mesma arrow function, porém como recebe apenas um argumento eliminamos os parênteses, e como era apenas uma linha retornando `true` or `false`, eliminamos a palavra return e alinhamos tudo em uma linha.