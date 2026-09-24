---
tipo: indice
status: ativo
tags: [umbanda/indice]
---

# Índice Geral

Painel dinâmico da base de estudos. As seções abaixo são geradas automaticamente pelo Dataview a partir das propriedades das notas.

## Estudos em andamento

```dataview
TABLE tema AS "Tema", revisado AS "Última revisão"
FROM ""
WHERE tipo = "estudo" AND status = "em-andamento"
SORT file.name ASC
```

## Orixás

```dataview
TABLE status AS "Status", revisado AS "Última revisão"
FROM "02 - Orixas"
WHERE tipo = "orixa"
SORT file.name ASC
```

## Conceitos

```dataview
TABLE status AS "Status", revisado AS "Última revisão"
FROM ""
WHERE tipo = "conceito"
SORT file.name ASC
```

## Guias espirituais

```dataview
TABLE linha AS "Linha", falange AS "Falange", status AS "Status"
FROM "05 - Guias Espirituais"
WHERE tipo = "guia-espiritual"
SORT file.name ASC
```

## Fontes

```dataview
TABLE autor AS "Autor", obra AS "Obra", ano AS "Ano", status AS "Status"
FROM "10 - Fontes"
WHERE tipo = "fonte"
SORT file.name ASC
```

## Mapas

```dataview
TABLE status AS "Status"
FROM "09 - Mapas"
WHERE tipo = "mapa"
SORT file.name ASC
```

## Notas para revisão

```dataview
TABLE tipo AS "Tipo", status AS "Status", revisado AS "Última revisão"
FROM ""
WHERE status = "estudo" OR status = "rascunho"
SORT file.name ASC
```

## Estatísticas da base

### Total de notas de conteúdo

```dataview
TABLE WITHOUT ID
length(rows) AS "Quantidade"
FROM ""
WHERE tipo
GROUP BY tipo AS "Tipo"
SORT Tipo ASC
```

> [!note]
> Este painel ficará mais útil conforme novas notas receberem propriedades padronizadas como `tipo`, `status`, `fontes` e `revisado`.
