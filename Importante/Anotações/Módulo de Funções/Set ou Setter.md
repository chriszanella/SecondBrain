---
tags:
  - palavra-chave
---


## 📅 Data da anotação
- Criado em: 2025-05-18
- Última revisão: 2025-05-18

---

## 🧠 Resumo rápido
- É uma palavra chave usada para **definir um setter**
- Função especial que é executada quando uma propriedade de um objeto é atribuída
> Como Por exemplo uma função dentro de um objeto com get. -> [[#Setter e um Getter]]
---

## 📌 Conceitos principais
- {{ Adiciona os principais pontos aqui }}
- 

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]
- [[Get ou Getter]]

---

## Anotações Rápidas e Importantes
- 

---

## 📖 Exemplos práticos
### Setter e um Getter
```js
const pessoa = {
	nome: 'Chris',
	sobrenome: 'Zanella',
	get nomeCompleto() {
		return `${this.nome} ${this.sobrenome}`
	}
	set nomeCompleto(valor) {
		valor = valor.split(' ');
		this.nome = valor.shift();
		this.sobrenome = valor.join(' ')

		// Aqui ele pega o valor passado pelo usuário, recorta a cada espaço vazio.
		// com o shifter, como ele mostra o primeiro valor do array e dai remove, primeiro valor.nome recebe o nome, dai ele exclui depois, dai na próxima linha de código o primeiro valor já não é mais o nome e sim o sobrenome e depois eu concateneo com o outro sobrenome.
	}
}
console.log(pessoa.nomeCompleto) // Mostra o nome completo -> Executa a função mas eu chamo como se fosse um atributo.

pessoa.nomeCompleto = 'Christian Zanella Silva' // Eu to adicionando um valor a propriedade "nomeCompleto", dai o set entra em ação.

console.log(pessoa.nome); // Christian
console.log(pessoa.sobrenome); // Zanella Silva
console.log(pessoa.nomeCompleto); // Christian Zanella Silva
```