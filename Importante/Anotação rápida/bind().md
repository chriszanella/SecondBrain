Dia :: 2025-05-20
### Anotação rápida
- Pode ser usado com o `this`, quando, Você quer alterar à o que se esta se referindo o `this`.
- Como quando tu está dentro de uma função e quer utilizar o `this` se referindo ao objeto na qual essa função está dentro, dessa maneira:
```js

function teste() {
	return {
	nome: 'Chris',
	sobrenome: 'Zanella',
	
	nomeCompleto() { //Esse é um método, this aqui, ainda se refere ao objeto do return.
	
	document.addEventListener('click', function(e) {
	if (e.target.classList.contains('.btn-num')) { // Aqui é uma função, na qual o this muda de referência e passa a se referir ao método.
	
	return `${nome} ${sobrenome}`
	
	}.bind(this) //No fim dessa função tu pode chamar o .bind(this)
	})
	}
	}
}

```
- Adicionando o `.bind(this)` no fim da função exemplificada acima, ele estará falando o seguinte pro `this`.:
	- Eu quero que você deixe de se ter o valor dai de dentro, e passe a ter o valor aqui de fora. 
	- Que significa que o `this` irá deixar de ter o significado que tem sendo ali de dentro( Que é se referir ao bloco do método), e passa a ter o significado que tem quando o `this` está dentro do próprio método( Que esta se referindo ao bloco em que o método está. )