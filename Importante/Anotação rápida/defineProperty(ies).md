Dia :: 2025-07-14
### Anotação rápida
- defineProperty é um método que utilizamos para configurar objetos
- EX:
```
Object.defineProperty(qual é o objeto, qual a chave do objeto a ser configurada, {aqui vai a configuracao do objeto})
```
- Como é a configuração:
```
Object.defineProperty(this, 'enquete', {
	enumerable: true // define se é mostrada ou nao em console e etc essa chave, como em Object.keys()
	value: enquete // valor que essa chave irá receber
	writable: true // Se o valor dessa chave pode ser alterado posteriormente
	configurable: true // Se essa chave pode ser reconfigurada posteriormente ou não.
})
```