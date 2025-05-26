Dia :: 2025-05-25
### Anotação rápida
- Ele recebe uma função de callback que irá iterar sobre cada um dos elementos do meu array. 
- Não modifica o array que filtrou, então tem que criar um outro array para receber o que ele filtrou
- Ele automaticamente passa 3 argumentos para a função de callback -> `function callbackFilter(valor, índice, array) {}`
	- `valor` -> É o valor mesmo que ta no array, por exemplo 5.
	- `índice` -> o índice desse valor, nesse caso 0.
	- `array` -> retorna o array inteiro.
- Ele funciona como um `for of` -> Passa pelo valor no índice 0, executa a função callback, depois pelo valor no índice 1, executa a funçã callback até o fim.