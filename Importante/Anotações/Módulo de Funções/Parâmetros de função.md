---
tags:
  - teoria
---
## 📅 Data da anotação

- Criado em: 2025-05-18
- Última revisão: 2025-05-18

---

## 🧠 Resumo rápido

- Parâmetros em funções JS podem ter **valores padrão**, ser **desestruturados**, ou ainda usar o **rest operator** pra agrupar valores restantes. 
- Isso dá muita flexibilidade pra montar funções mais inteligentes e reaproveitáveis.

---

## 📌 Conceitos principais

- Parâmetros com valor padrão só são usados se o valor passado for `undefined`.

- Argumentos `falsy` como `0`, `''` ou `null` **ainda são considerados válidos** e **substituem** o valor padrão.

- Dá pra desestruturar objetos ou arrays direto nos parâmetros.

- O operador de resto (`...`) junta os argumentos restantes num array.

---

## 🧩 Conexões com outros temas

- [[Painel Funções]]

---

## Anotações Rápidas e Importantes

- `undefined` ativa o valor padrão. Qualquer outro valor (mesmo `0` ou `''`) **desativa o default**.

- `null` é tratado como valor normal — se somar, entra como `0`.

- Desestruturação nos parâmetros ajuda a deixar o código limpo e legível.

- O operador `...rest` deve ser o **último parâmetro da função**.

---

## 📖 Exemplos práticos

### Parâmetros com valor padrão

```js
function funcao(a, b = 2, c = 4) {
	console.log(a + b + c); 
} 
funcao(2, 0, 20); // 2 + 0 + 20 = 22`
```
> Mesmo `0` sendo falsy, ele **ainda vale como argumento válido**, então **o valor padrão não é usado**.

---

### Forçando o uso do valor padrão

```js
function funcao(a, b = 2, c = 4) {
	console.log(a + b + c);
};
funcao(2, undefined, 20); // b usa o valor padrão = 2 → 2 + 2 + 20 = 24
```
> **Somente `undefined` ativa o valor padrão.**  
> `null` conta como argumento e entra no cálculo → vira `0`.

---

### Parâmetros por desestruturação
```js
function funcao({ nome, sobrenome, idade }) {
	console.log(nome, sobrenome, idade);
};
let obj = {
	nome: 'Chris',
	sobrenome: 'Zanella',
	idade: 18
};
funcao(obj);
```

**O que rola aqui:**

- A função espera um objeto com as chaves `nome`, `sobrenome` e `idade`.

- Ela **desestrutura direto nos parâmetros**, extraindo os valores e criando variáveis.    

---

### Desestruturação com arrays
```js
function funcao([a, b, c]) {
	console.log(a, b, c);
}
let arr = [1, 2, 3]; funcao(arr); // 1 2 3
```

---

### Rest operator (`...`) nos parâmetros

```js
function conta(operador, acumulador, ...numeros) {
console.log(operador, acumulador, numeros);
};
conta('+', 0, 10, 20, 30, 40, 50);
```
> O `...numeros` pga **todo o resto dos argumentos** e transforma nuem array.  
> Aqui, `operador = '+'`, `acumulador = 0`, e `numeros = [10, 20, 30, 40, 50]`.