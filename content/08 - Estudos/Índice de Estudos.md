---
tipo: indice
status: ativo
tags: [umbanda/indice, umbanda/estudo]
---

# Índice de Estudos

## Formação

- [[Trilha de Formação]] — percurso progressivo organizado em 22 módulos.

### Aulas da formação

```dataview
TABLE modulo AS "Módulo", aula AS "Aula", status AS "Status", revisado AS "Revisado"
FROM "08 - Estudos/01 - Formação"
WHERE tipo = "aula"
SORT modulo ASC, aula ASC
```

## Estudos temáticos em andamento

```dataview
TABLE tema AS "Tema", iniciado AS "Iniciado", revisado AS "Revisado"
FROM "08 - Estudos/02 - Estudos Temáticos"
WHERE tipo = "estudo" AND status = "em-andamento"
SORT file.name ASC
```

## Todos os estudos temáticos

```dataview
TABLE status AS "Status", tema AS "Tema", revisado AS "Revisado"
FROM "08 - Estudos/02 - Estudos Temáticos"
WHERE tipo = "estudo"
SORT file.name ASC
```

## Trilhas complementares

- [[Índice de Estudos de Ervas|Estudos de Ervas]]
- [[Índice do Catálogo de Ervas|Catálogo de Ervas]]

> [!note]
> As aulas organizam a sequência pedagógica. As notas das demais áreas do Vault continuam sendo a base conceitual e devem ser ligadas pelas aulas em vez de duplicadas.
