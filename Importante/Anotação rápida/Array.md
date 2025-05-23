Dia :: 2025-05-23
### Anotação rápida
- [] - Array Literal;
- Podemos criar um array da seguinte forma:
```js
const array = new Array('Valor 1', 'Valor 2', 'Valor 3');
```
- o `delete`, pode ser usado para deletar um índice em um array, deixando um "furo", pois fica constando: `<! empty item >`;
- `.pop()` - remove o último valor e retorna ele, podendo fazer a remoção e ao mesmo tempo atribuindo a uma variável, deixando o valor salvo:
```js
const nomes = ['Christian', 'Joaquim', 'Júlio'];
const name = nomes.pop() // Remove 'Júlio' e retorna ele, adicionando a essa variável.

console.log(nomes) // ['Christian', 'Joaquim']
console.log(name) // 'Júlio'
```
- `.shift()` - Remove o primeiro elemento, e como o `.pop()`, ele retorna o que removeu.
- `.push()` - Adiciona o que quiser ao final da array:
```js
const nomes = ['Christian', 'Joaquim'];
nomes.push('Júlio')

console.log(nomes) // ['Christian', 'Joaquim', 'Júlio']
```
- `.unshift()` - Adiciona o que quiser no início do array. Similar ao `.push()`, porém agora no início do array( move todos os outros para o próximo índice )