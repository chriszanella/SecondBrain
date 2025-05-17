Nada mais nada menos é que a função entende aonde ela ta, se eu tento mostrar o valor de uma variável, primeiro ela irá verificar o seu bloco se tem, caso nao tenha, vai procura no escopo do seu pai(lado de fora dela), caso nao tenha no lado de fora do bloco de seu pai(pai do seu pai -> avo), e assim por diante até chegar no escopo global que caso não tenha, retorna erro.

<i>Obs: uma função tem acesso a tudo do lado de fora dela e dentro do seu próprio bloco, porém, não pode acessar o bloco de outra função, exemplo:</i>

```js
const nome = 'Chris';
function falaNome() {
	console.log(nome)
}
```
Funciona, irá mostrar -> `Chris`.

Agora:

```js
function falaNome() {
	console.log(nome)
}
function armazenaNome(){
	const nome = 'Chris'
}
```
Da erro, pois, a função buscou em seu bloco a variável nome e não encontrou, procurou no seu pai e não encontrou, como se não tinha mais aonde buscar, retorna erro.

isso tudo, mesmo dentro da função -> `armazenaNome()`, ter uma variável com o nome.
