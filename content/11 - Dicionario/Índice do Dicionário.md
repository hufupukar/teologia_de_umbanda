---
tipo: indice
status: ativo
tags: [umbanda/indice, umbanda/dicionario]
---
# Índice do Dicionário

> [!abstract]
> O dicionário registra termos africanos, afro-brasileiros, umbandistas, rituais e tradicionais. **Grafia brasileira, forma na língua de origem, etimologia e significado religioso são campos diferentes** e não devem ser fundidos.

## Todos os verbetes

```dataview
TABLE aliases AS "Variantes", status AS "Status"
FROM "11 - Dicionario"
WHERE tipo = "termo"
SORT file.name ASC
```

## Termos em revisão

```dataview
TABLE aliases AS "Variantes", fontes AS "Fontes"
FROM "11 - Dicionario"
WHERE tipo = "termo" AND status != "consolidado"
SORT file.name ASC
```

## Critérios do dicionário
Cada verbete deve, quando as fontes permitirem, separar:

**termo → forma linguística → variantes → significado lexical → significado religioso → uso na Umbanda → uso em outras tradições → divergências → fontes.**

Uma etimologia incerta permanece explicitamente incerta.

## Eixos atuais
- línguas e matrizes africanas;
- nomes de Orixás;
- saudações;
- funções e cargos;
- ritualística;
- organização espiritual;
- mediunidade;
- tradição oral.

## Relações
- [[Índice de Fontes]]
- [[Orixás]]
- [[Linhas e Falanges]]
- [[Guias Espirituais]]
- [[Ritualística]]
