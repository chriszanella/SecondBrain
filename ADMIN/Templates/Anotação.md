---
tags:
---

<%*
const assunto = await tp.system.prompt("Qual é o assunto dessa nota?");
const dataHoje = tp.date.now("YYYY-MM-DD");
const data3dias = tp.date.now("YYYY-MM-DD", 3);
const data7dias = tp.date.now("YYYY-MM-DD", 7);
%>
## 📅 Data da anotação
- Criado em: <% dataHoje %>
- Última revisão: <% dataHoje %> | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
<!-- Explica em até 3 frases o que é o assunto e por que ele é importante. -->

---

## 📌 Pontos Importantes
- {{ Adiciona os principais pontos aqui }}
- 

---

## 🧩 Conexões com outros temas
- <!-- Linkar com painel principalmente -->

---

## 📖 Exemplos práticos
```js
// Exemplo prático de aplicação do conteúdo
```