Armazena o escopo da função externa na memória para que a função interna possa acessar.

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
