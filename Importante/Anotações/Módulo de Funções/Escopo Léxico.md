---
tags:
  - teoria
---
## 📅 Data da anotação

- Criado em: 2025-05-18
- Última revisão:  2025-05-18 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido

- A palavra-chave `this` **representa o contexto atual de execução**.  
- Ela muda dependendo de como e onde a função é chamada. **Não depende de onde a função foi criada**, e sim de **como ela é chamada**.

---

## 📌 Conceitos principais

- `this` pode apontar para o `window`, um `objeto`, uma `classe`, etc.

- Em funções tradicionais, `this` varia conforme a **forma da chamada**.

- Em arrow functions, `this` **herda do escopo onde foi criada**.

- Dentro de métodos de objeto, `this` aponta pro objeto.

- Fora de qualquer função, `this` aponta pro escopo global (`window` no navegador).

---

## 🧩 Conexões com outros temas

- [[Painel Funções]]

---

## Anotações Rápidas e Importantes

- `this` em funções normais é **dinâmico**: depende de como foi chamada.

- `this` em arrow functions é **fixo**: não muda, é herdado do pai.

- Se usar uma função como callback em eventos ou métodos, o `this` pode ser **quebrado** (não apontar pro objeto certo).

- Dá pra "corrigir" o `this` usando `.bind()`, `.call()`, ou `.apply()`.

---

Beleza, agora entendi o que tu quis dizer. Tu quer que **todos os blocos de código** estejam com a **formatação perfeita**, tipo identado bonitinho, com comentários na linha certa, e tudo cercado com ` ```js ` e ` ``` `, no estilo que o Obsidian (ou Discord) entende.

Aqui vai o conteúdo sobre `this` **corrigido e formatado como tu pediu**:

---

## 📖 Exemplos práticos

### 🔹 Fora de qualquer função

```js
console.log(this); // No navegador: Window
```

---

### 🔹 Dentro de uma função normal

```js
function mostrarThis() {
	console.log(this);
}
mostrarThis(); // No modo não estrito: Window (ou globalThis fora do navegador)
```

---

### 🔹 Dentro de um objeto

```js
const obj = {
	nome: 'Chris',
	falar() {
		console.log(this.nome);
	}
};

obj.falar(); // Chris
```

---

### 🔹 Dentro de uma arrow function

```js
const obj = {
	nome: 'Chris',
	falar: () => {
		console.log(this.nome);
	}
};

obj.falar(); // undefined (arrow function não tem seu próprio `this`)
```

---

### 🔹 Fixando o `this` com bind

```js
function falar() {
	console.log(this.nome);
}

const pessoa = {
	nome: 'Zanella'
};

const falarNome = falar.bind(pessoa);
falarNome(); // Zanella
```

---

### 🔹 Arrow function herdando `this` do pai

```js
const pessoa = {
	nome: 'Chris',
	falar() {
		const arrow = () => {
			console.log(this.nome);
		};
		arrow();
	}
};

pessoa.falar(); // Chris
```

---

### 🔹 Exemplo com escopo léxico

```js
const nome = 'Chris';

function falaNome() {
	console.log(nome);
}

falaNome(); // Chris
```

Mas se a variável estiver em outro bloco:

```js
function falaNome() {
	console.log(nome);
}

function armazenaNome() {
	const nome = 'Chris';
}

falaNome(); // ReferenceError: nome is not defined
```

> Mesmo que `armazenaNome()` tenha um `nome`, **`falaNome` não enxerga**, pois está em outro escopo.
