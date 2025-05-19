---
tags:
  - Painel
---

## Resumo do que acessa.
- Tipos de funções
- Teorias e/ou Definições
- Palavras Chave

---

## Quais Ligações

### Tipos de Função
```dataview
table file.name as "Tipo de Função"
from "Importante/Anotações"
where contains(tags, "tipo-de-função")
sort file.mtime desc
```

### Teoria/Definições
```dataview
table file.name as "Teoria/Definições"
from "Importante/Anotações"
where contains(tags, "teoria")
```

### Palavras Chave
```dataview
table file.name as "Palavras Chave"
from "Importante/Anotações"
where contains(tags, "palavra-chave")
```