---
tags:
  - tipo-de-função
---

## 📅 Data da anotação
- Criado em: 2025-05-18
- Última revisão: 2025-05-18

---

## 🧠 Resumo rápido
**IIFE** é uma função que tu **declara e já executa na hora**, sem precisar chamar depois.. E serve para guardar-estado, armazenar dados privados, implementar, debounce/throttle/cache e modularizar lógica.

---

## 📌 Conceitos principais
- {{ Adiciona os principais pontos aqui } 

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]

---

## Anotações Rápidas e Importantes
- 

---

## 📖 Exemplos práticos
```js
(function(){
	console.log('Olá mundo!');
})();

// Funciona com arrow function também

(() => {
	console.log('Olá mundo!');
})():
```
> // Isso já roda **imediatamente**. Tu não precisa chamar com nome nem nada.