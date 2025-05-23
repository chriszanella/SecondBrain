---
tags:
  - tipo-de-função
---


## 📅 Data da anotação
- Criado em: 2025-05-22
- Última revisão: 2025-05-22 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
- Ela mesmo chama a si mesma.
- Ela faz a execução dela com um chamado simples, e se chama.
- Exemplo de função recursiva -> [[#Recursividade - Simples]]

---

## 📌 Pontos Importantes
- Motor do Javascript possui uma limitação de recursividade, por isso definimos um limite de máximo.

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]

---

## 📖 Exemplos práticos
#### Recursividade - Simples
```js
function recursiva(max) {
	if (max > 10) return;
	max++;
	console.log(max);
	recursiva(max);
}
recursiva(1)
```
> O que acontece acima? 
- `recursiva(1)` -> A função é chamada uma primeira vez com um argumento passado 
- `if (max > 10) return` -> Irá verificar se o argumento passado é menor que 10, que se for, para no return que fecharia o bloco da função.
- `max++` -> Adiciona um ao valor do argumento.
- `console.log(max)` -> Mostra na tela.
- `recursiva(max)` -> E chama ela mesma, passando o valor atual de `max` que agora esta com +1 do passado primordialmente.
- Ela fica executando e mostrando na tela o valor de `max` atual até que `max` fique com um valor acima de 10