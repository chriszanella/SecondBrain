---
tags:
  - palavra-chave
---


## 📅 Data da anotação
- Criado em: 2025-05-22
- Última revisão: 2025-05-22 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido
Usado dentro de funções geradoras para falar o que será retornado daquela função

---

## 📌 Pontos Importantes
- Pode ser usado mais de uma vez na mesma função, diferente do `return`
- Pode ser usado assim -> `yield*`, servindo para "delegar", usar os `yield` da função chamada, fica assim -> [[#Yield*]]
- `yield*` -> Entrega TODOS os valores de outro iterável

---

## 🧩 Conexões com outros temas
- [[Funções Geradoras]]

---

## 📖 Exemplos práticos
#### Yield*
```js
function* parte1() {
  yield 1;
  yield 2;
}

function* parte2() {
  yield 3;
  yield 4;
}

function* tudoJunto() {
  yield* parte1(); // delega pra parte1
  yield* parte2(); // delega pra parte2
  yield 5;         // valor individual
}
```
> O que acontece?
- É criado a parte um que tem dois `yields` que retornam valor 1 e 2.
- Criado a parte dois que retorna 3 e 4.
- E dai criado a função construtora principal, que vai chamar elas usando `yield*`, no qual seria como pegar os `yields` da função que ta sendo usada por ele, e jogar dentro da função aonde eles estão.

**O resultado abaixo:**
```js
for (const valor of tudoJunto()) {
  console.log(valor);
}
// Saída: 1 2 3 4 5
```
	- Criado um loop for para mostrar o valor cada vez que executar a função.