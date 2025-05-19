---
tags:
  - teoria
---


## 📅 Data da anotação
- Criado em: 2025-05-18
- Última revisão: 2025-05-18

---

## 🧠 Resumo rápido
- Uma **closure** é quando uma função **lembra do escopo onde ela foi criada**, mesmo depois desse escopo já ter “acabado”.
- Isso permite que a função use variáveis de fora dela, **mesmo depois da função externa já ter sido executada**.

---

## 📌 Conceitos principais
- {{ Adiciona os principais pontos aqui }}
- 

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]

---

## Anotações Rápidas e Importantes
- 

---

## 📖 Exemplos práticos

**Por que esse código não zera o contador a cada clique?**
```js
function contador() {
  let count = 0;
  return () => {
    count++;
    console.log(count);
  };
}
const contar = contador();
botao.onclick = contar;
```
Resposta: Pois a função interna lembra do seu escopo e do seu pai([[Closure]]) e o count fica preservado a cada clique.