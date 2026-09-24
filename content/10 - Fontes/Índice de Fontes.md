---
tipo: indice
status: ativo
tags: [umbanda/indice, umbanda/fonte]
---

# Índice de Fontes

Uma nota por obra, nomeada **"Autor - Obra"**. Obras de referência sem autor individual (dicionários, sites) usam o nome da obra ou da instituição. As notas de conteúdo citam as fontes no campo `fontes:` como link, e cada nota de fonte lista automaticamente quem a cita.

## Biblioteca pessoal

```dataview
TABLE autor AS "Autor", ano AS "Ano", perspectiva AS "Perspectiva", escola AS "Escola", status AS "Status"
FROM "10 - Fontes"
WHERE tipo = "fonte" AND biblioteca = true
SORT file.name ASC
```

## Obras acadêmicas, documentos e outras obras citadas

```dataview
TABLE autor AS "Autor", ano AS "Ano", tipo-fonte AS "Tipo", perspectiva AS "Perspectiva"
FROM "10 - Fontes"
WHERE tipo = "fonte" AND biblioteca != true AND perspectiva != "referência"
SORT file.name ASC
```

## Obras de referência

```dataview
TABLE tipo-fonte AS "Tipo"
FROM "10 - Fontes"
WHERE tipo = "fonte" AND perspectiva = "referência"
SORT file.name ASC
```

## Fontes mais citadas

```dataview
TABLE length(file.inlinks) AS "Notas que citam"
FROM "10 - Fontes"
WHERE tipo = "fonte"
SORT length(file.inlinks) DESC
LIMIT 15
```
