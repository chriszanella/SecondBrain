---
tags:
  - tipo-de-função
---


## 📅 Data da anotação
- Criado em: 2025-05-21
- Última revisão: 2025-05-22 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
Function construtora é um jeito clássico de criar vários objetos parecidos, tipo um molde. Imagina que tu quer fazer várias “coisas” do mesmo tipo, com propriedades e métodos iguais, sem ter que ficar repetindo tudo do zero. A function construtora é o molde que gera esses objetos.

---

## 📌 Pontos Importantes
- Cria a função com nome maiúsculo para na hora da chamada perceber-se que é construtora
- sempre vai ser chamada com o `new`antes -> `function Pessoa(){}` -> `const chris = new Pessoa()`
- usando: `this.name`(por exemplo.) Está criando um atributo ou método público.
- Pode criar "variáveis" dentro, que são chamadas de Atributos ou Métodos Privados.
- retorna tudo(à função), como se fosse um objeto, sem precisar que retorne utilizando o `return`.

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]

---

## 📖 Exemplos práticos
```js
function Pessoa(nome, idade) {
  this.nome = nome;    // aqui tu cria a propriedade nome no objeto que vai ser criado
  this.idade = idade;  // mesma coisa pra idade
  this.falar = function() {
    console.log(`Meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  };
}

// Criando objetos com a function construtora
const christian = new Pessoa('Christian', 16);
const maria = new Pessoa('Maria', 20);

christian.falar(); // Meu nome é Christian e tenho 16 anos.
maria.falar();     // Meu nome é Maria e tenho 20 anos.
```

### O que rola aqui:
- A função Pessoa é o molde.
- this aponta pro objeto que vai ser criado.
- new Pessoa(...) cria um objeto novo usando esse molde.
- Cada objeto criado tem suas próprias propriedades e métodos.