Se formos criar funções para duplicar, triplica etc algum número se torna repetitivo.:
```js
function duplica(n) {
	return n * 2
}
function triplica(n) {
	return n * 3
}
function quadriplica(n) {
	return n * 4
}

console.log(duplica(2)) // 4
console.log(triplica(2)) // 6
console.log(quadriplica(2)) // 8

```

Podemos criar um função que recebe  um multiplicador e essa função retorna uma outra função que recebe um número e multiplica pelo multiplicador.
```js
function criarMultiplicacao(multiplicador) {
	return function(n) {
		return n * multiplicador
	}
}

const duplica = criarMultiplicacao(2);
const triplica = criarMultiplicacao(3);
const quadriplica = criarMultiplicacao(4);

console.log(duplica(2)); // 4
console.log(triplica(2)); // 6
console.log(quadriplica(2)); // 8

```
> criamos variáveis na qual passamos qual vai ser o multiplicador, e se chamarmos ela como função, estaremos definindo o número e será retornado o resultado.

**Como isso funciona? `// damos exemplo usando duplicar`**
	1- Ao chamarmos a função de `criarMultiplicacao` e passamos um argumento, a função cria a variável com o parâmetro e o seu valor. <span style="background:rgba(5, 117, 197, 0.2)">(multiplicador agora equivale a 2)</span>
	-
	2- retorna uma função e essa função recebe um número e multiplica pelo multiplicador<span style="background:rgba(136, 49, 204, 0.2)">(variável criada e recebida pela função maior, e como uma função pode acessar todas as variáveis ao seu redor, funciona.)</span>
	-
	3- Como a função -> `criarMultiplicacao()`, retorna uma variável sem executar ela, se eu atribuir ela a uma variável seria igual eu criar uma função sem nome como valor de uma variável -> `function expression.` - > [[function expression]]
	-
	4- quando eu chamar o nome da variável como função, passando um valor de um número para o cálculo, ele estará executando aquela função que faz o calculo. e retorna o resultado agora. <span style="background:rgba(5, 117, 197, 0.2)">(duplicar(2) // retorna 2 * 2 = 4)</span>

---
