---
aliases:
  - Gerenciador Global de Painéis e Informações.
---
## Links importantes
- <font color="#b2a2c7">Como instalar e configurar o WakaTime no seu perfil</font>
> https://github.com/orgs/community/discussions/115279

---

## Senhas//Tokens
- [[🗿 Senhas]]

---

## Paineis
#### Geral
```dataview
table file.name as "Painéis"
from "ADMIN/Painéis"
where contains(tags, "Painel")
```

---

## Linkar
- [[Linkador de Templates]]
- [[Linkador de Datas]]
- [[Linkador de Painéis]]

---

## Estudos
- Html
- CSS
- TailwindCSS
- Javascript

---

### 🚀 Projetos Ativos
```dataview
table file.name, tags, status
from "Importante/Projetos"
sort file.mtime desc
```