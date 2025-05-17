Segue o código:
```js
function funcao(a, b = 2, c = 4) {
console.log(a + b + c);
}
funcao(2, 0 /* ou '' */, 20)
```
> Os valores de B e de C já tem valor padrão, para caso eu nao sete seus valores, porém, se eu quiser setar um valor para C e usar o padrão no B, nem argumentos que retornariam false funcionam, apenas se eu setar undefined, assism:
```js
function funcao(a, b = 2, c = 4) {
console.log(a + b + c);
}
funcao(2, undefined, 20);
```
> Assim funcionaria, mas se ao acaso eu pensasse em usar 0, ou ''(string vazia), que ambos retornam falsy. nao funcionaria, o 0 equivaleria a número e B seria = a 0, e a string vazia faria com que concatenasse os 3 valores.
> Se eu passar null no segundo argumento, a função levaria como 0. não somando na conta. 



### Parâmetros por desestruturação
Posso utilizar a desestruturação como parâmetro da seguinte forma:
```js
function funcao({nome, sobrenome, idade}) {
		console.log(nome, sobrenome, idade)
}
let obj = {nome: 'Chris', sobrenome: 'Zanella', idade: 18}
funcao(obj);
```
Detalhando o que esta acontecendo:
- A função tem como parâmetros um object.
- Ao chamar a função estou passando outro objeto
- Ela analisa e atribui na variável NOME o valor: 'Chris', SOBRENOME o valor: 'Zanella' e na variável IDADE o valor: 18.
Desestruturando o object.

Funciona da mesma maneira com arrays. porém, você pode definir o nome da variável mais facilmente.

---
operador, acumulador, números usando 'rest operator'

Agora, foi falar sobre operador de resto dando exemplo de uma função que você passa como argumento um operador, um acumulador e os números, que pode passar um array e etc. da seguinte maneira;
```js
function conta(operador, acumulador, numeros) {
	console.log(operador, acumulador, numeros);
}
conta('+', 0, [10, 20, 30, 40, 50]) // Utilizando array.
```

Mas, melhor.. uma forma mais fácil de se obter esses valores é utilizando o operador de resto, pois eu quero bem definido o operador, e o acumulador, dai com o resto dos números, seja feito a conta.

- Operador de resto: `...variável` -> `...numeros` - pega o resto.
- Ele armazena o resto dentro de um array.

Ficaria assim dai:
```js
function conta(operador, acumulador, ...numeros) {
	console.log(operador, acumulador, numeros)
}
conta('+', 0, 10, 20, 30, 40, 50) // Usando operador de resto.
```