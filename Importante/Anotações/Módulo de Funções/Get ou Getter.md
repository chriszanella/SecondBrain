---
tags:
  - palavra-chave
---


## 📅 Data da anotação
- Criado em: 2025-05-18
- Última revisão: 

---

## 🧠 Resumo rápido
a palavra chave `get` serve para <font color="#3f3151">criar propriedades que se comportam como variáveis</font>, mas na real são funções por trás dos panos.

---

## 📌 Conceitos principais
- Usado para chamar funções como se chama um atributo padrão dentro de um objeto. [[#Como Chamar]]
- 

---

## 🧩 Conexões com outros temas
- [[Painel Funções]]
- [[Set ou Setter]]

---

## Anotações Rápidas e Importantes
- 

---

## 📖 Exemplos práticos
### Como Chamar
O trecho de código abaixo cria um object e dentro desse object tem uma função que cria o nome completo.
```js
	const p1 = {
		nome: 'chris',
		sobrenome: 'zanella',
		get nomeCompleto() {
			return `${nome} ${sobrenome}`
		}
		// Sem o get eu chamaria assim:
		console.log(p1.nomeCompleto());

		//Com o get antes fica assim:
		console.log(p1.nomeCompleto);

	}
```

##### Pontos importantes
- o get vai antes da função para simbolizar que é aquela função
- ele executa como uma função, mas, se comporta como um atributo
		Inclusive se você definir o get  e tentar chamar como se chama uma função da erro retornando que aquilo não é uma função.
