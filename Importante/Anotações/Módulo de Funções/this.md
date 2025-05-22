---
tags:
  - palavra-chave
---

## 📅 Data da anotação
- Criado em: 2025-05-18
- Última revisão: 2025-05-20 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
`this` vai ser quem chamar o objeto.

---

## 📌 Pontos Importantes
- Se refere ao objeto pai do seu escopo em que foi chamado.
- Arrow Function Não muda o valor do this. (Funcionaria igual ao [[bind()]])

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]
- [[bind()]]

---

## 📖 Exemplos práticos
```js
const user = {
  nome: 'Christian',
  falar() {
    console.log(this.nome);
  }
};

user.falar(); // 'Christian'
```
