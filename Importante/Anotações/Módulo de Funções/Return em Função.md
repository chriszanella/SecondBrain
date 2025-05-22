---
tags:
  - teoria
---
## 📅 Data da anotação

- Criado em: 2025-05-18
- Última revisão: 2025-05-18 | **( Não esquecer de atualizar!!! )**

---

## 🧠 Resumo rápido

- A palavra-chave `return` serve pra finalizar uma função e devolver um valor. Mas esse valor pode ser **qualquer coisa**, número, string, objeto, até **outra função**.  
- Esse poder permite criar funções mais dinâmicas e reutilizáveis.

---

## 📌 Conceitos principais

- `return` encerra a execução de uma função e devolve um valor.

- Pode retornar funções → isso permite criar funções personalizadas na hora.

- Cria _closures_ quando a função retornada usa variáveis da função que a criou. [[#Como funciona o retorno de função]]

---

## 🧩 Conexões com outros temas

- [[Painel Funções]]
---

## Anotações Rápidas e Importantes

- Sem `return`, a função retorna `undefined` por padrão.
    
- Tudo que vem **depois** do `return` é ignorado na execução.
    
- Quando uma função retorna outra, não está executando ela ainda. Só está entregando a “receita” pra ser usada depois.
    
- A função retornada ainda **lembra** do que rolou na função onde ela nasceu (isso é closure).
    

---

## 📖 Exemplos práticos

### Repetição desnecessária

Criação de várias funções parecidas sem reaproveitamento:

```js
function duplica(n) {
	return n * 2;
}
function triplica(n) {
	return n * 3;
}
function quadriplica(n) {
	return n * 4;
}

console.log(duplica(2));      // 4
console.log(triplica(2));     // 6
console.log(quadriplica(2));  // 8
```

---

### Retornando uma função com `return`

Aqui entra o conceito forte de `return` devolvendo **uma função completa**:

```js
function criarMultiplicacao(multiplicador) {
	return function(n) {
		return n * multiplicador;
	}
}
```

---

### Aplicação prática

```js
const duplica = criarMultiplicacao(2);
const triplica = criarMultiplicacao(3);
const quadriplica = criarMultiplicacao(4);

console.log(duplica(2));      // 4
console.log(triplica(2));     // 6
console.log(quadriplica(2));  // 8
```

---

### Como funciona o retorno de função

1. Quando executa `criarMultiplicacao(2)`, ele **retorna uma função**, sem executar ainda.

2. Essa função retornada “lembra” que o `multiplicador` era `2`.

3. Quando você chama `duplica(2)`, ela executa a função retornada, usando o `multiplicador` que ela lembra.

4. Isso é possível porque funções no JS têm acesso ao escopo onde foram criadas ([[Closure]]).