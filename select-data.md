# Selecionar dados de uma coluna específica. (`SELECT`)

## Índice:
- Para que serve a declaração `SELECT`.
- Como especificar colunas.
- Explicando como usar a declaração.
- Comparação entre a tabela completa e a que selecionamos colunas específicas.

---
---

## Declaração `SELECT`

A declaração `SELECT` serve para selecionar colunas específicas da tabela sem a necessidade de mostrar todas elas na tela. Serve para manipular os dados de forma mais organizada.

## Como especificar colunas

Para especificar colunas, é necessário especificar o campo correspondente. <br> Exemplo abaixo:

```sql
SELECT brand, year FROM cars;
```
## Explicando o uso da declaração

A declaração `SELECT` precisa vir antes dos campos que deseja selecionar, e depois especificar de qual tabela são aqueles campos. No caso, os campos serão `brand` e `year` da **tabela *cars*.**

Exemplo abaixo.

```sql
SELECT brand, year FROM cars;
```

O que deve retornar o seguinte:

| brand  | year |
| ------ | ---- |
| Ford   | 1964 |
| Volvo  | 1968 |
| BMW    | 1978 |
| Toyota | 1975 |
(4 registros)

---

Originalmente, a tabelas anterior tem três campos: `brand`, `model` e `year`. Mas, nós selecionamos somente os campos `brand` e `year`. <br>

Abaixo como ela é originalmente:

| brand  | model   | year |
| ------ | ------- | ---- |
| Ford   | Mustang | 1964 |
| Volvo  | p1800   | 1968 |
| BMW    | M1      | 1978 |
| Toyota | Celica  | 1975 |
(4 registros)

Como ela é depois de selecionada as colunas `brand` e `year`: 

| brand  | year |
| ------ | ---- |
| Ford   | 1964 |
| Volvo  | 1968 |
| BMW    | 1978 |
| Toyota | 1975 |
(4 registros)
