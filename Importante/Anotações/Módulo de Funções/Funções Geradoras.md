---
tags:
  - tipo-de-função
---
	

## 📅 Data da anotação
- Criado em: 2025-05-22
- Última revisão: 2025-05-23 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
Função que pode fazer "pausas".. E a cada vez que chamar ela retornar um valor definido.

---

## 📌 Pontos Importantes
- na criação ao invés de apenas `function nome(){}`, agora utiliza-se um `*`, ficando da seguinte forma: `function* nome(){}`
- Usa-se [[yield]]
- Mostrando no console retorna: `Object [Generator]`
- Usando o método `.next()`, para  verificar o próximo valor retornado(`yield`) -> [[#Usando next()]]
- 

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]

---

## 📖 Exemplos práticos
#### Usando next()
```js
function* geradora1 () {
	yield 'Valor 1';
	yield 'Valor 2';
	yield 'Valor 3';
}
const g1 = geradora1();
console.log(g1.next().value) //Mostra { value: 'Valor 1', done: false }
```
- O `next()`, nada mais é do que um método que funções construtoras possuem, ele retorna um objeto com dois atributos importantes.
	- **Value:** Seu valor nada mais é do que o `yield`está retornando.
	- **Done:** Ele fala (com true or false), se é o ultimo valor a ser retornado ou não, como ali é o primeiro, retorna false(Não é o último a ser )
- Como ele retorna um objeto, se eu quiser mostrar apenas o valor de um dos dois atributos posso apenas chamar ele normalmente, como fiz ali após o `next()`, pedindo para ele me mostrar o valor do atributo `value` -> `console.log(g1.next().value`
- o atributo `done`, vai ficar true apenas quando executar uma vez que já não tem mais retorno de nada, como por exemplo, nesse caso, uma quarta vez. No qual o objeto retornado seria -> `{ value: undefined, done: true }`.

#### Fazendo iteração com For
```js
function* geradora1 () {
	yield 'Valor 1';
	yield 'Valor 2';
	yield 'Valor 3';
}
const g1 = geradora1();
for (let valor of g1) {
	console.log(valor)
}
```
- É retornado cada valor corretamente.
- O for sabe exatamente os valores e sabe quando termina.
*A saída seria algo assim:*
```node
Valor 1
Valor 2
Valor 3
```

#### Gerador infinito
Podemos criar um gerador infinito, no qual sempre que chamarmos ele retorna um número maior -> 0,1,2,3,4,5,6,7,8,9 | infinito.
```js
	function* contador() {
		let i = 0;
		while(true) {
			yield i;
			i++;
		}
	}
	const contador = contador()
```
> Isso nada mais faz o que?
- Cria uma variável de controle no contador.
- Faz um Loop Infinito que "retorna" o valor da variável de controle e adiciona um após isso.

> Ou seja, sempre que chamarmos o contador assim -> `console.log(contador.next().value)`, ele irá retornar +1 número. 

- primeiro mostrará o 0, pois ele mostra antes de adicionar. 
	- ####