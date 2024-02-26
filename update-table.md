# Atualizar dados de tabelas
## Índice:
- Para o que serve
- Explicando a sintaxe da declaração `UPDATE`
- Atualizando uma coluna
- Atualizando múltiplas colunas

## Para o que serve a declaração `UPDATE`
A declaração `UPDATE` serve para adicionar dados em valores de campos específicos de uma coluna da tabela.

## Explicando a sintaxe da declaração `UPDATE`

A declaração `UPDATE` vem com duas declarações, são elas: **SET e WHERE**, estas duas declarações se comunicam entre si, pois as duas se complementam para atualizar dados da tabela. 

**A declaração `UPDATE`** serve para indicar ao PostgreSQL qual tabela será atualizada.

**A declaração **SET**** especifica um campo da tabela e adiciona um valor a tal campo.

**A declaração **WHERE**** especifica em qual outro campo será adicionada a mudança de valor feita usando a declaração **SET**. <br> Exemplo abaixo:

```sql
UPDATE cars
  SET color = 'red'
  WHERE brand = 'Volvo';
```

Entenda o código acima, a declaração *SET* especificou o campo já existente "color" e adicinou a cor "red" ao campo "color". A declaração *WHERE* especifica em qual campo outro campo será adicionado o valor "red" declarado com a declaração *SET*.

Resultado:

```
| brand  | model   | year | color |
| ------ | ------- | ---- | ----- |
| Ford   | Mustang | 1964 |       |
| BMW    | M1      | 1978 |       |
| Toyota | Celica  | 1975 |       |
| Volvo  | p1800   | 1968 | red   |
```

A declaração **SET** especificou o campo "color" e a declaração **WHERE** indicou que o valor dado ao campo "color" com a declaração **SET** vai ser adicionado ao campo "brand" cujo o valor é "Volvo".


---
# AVISO IMPORTANTE:
## Tenha cuidado ao atualizar colunas. Se você não usar a declaração `WHERE`, TODOS os dados serão atualizados em todos os campos! <br> Então não esqueça de usar a declaração `WHERE` para sinalizar aonde você quer aplicar as atualizações. 

## EXEMPLO: No código abaixo, sem a declaração `WHERE`, TODOS os campos serão atualizados a partir somente da declaração `SET`.

```sql
UPDATE cars
  SET color = 'red';
```
---
## Atualizando múltiplas colunas

Para atualizar mais de uma coluna, separe os campos e valores com uma vírgula.

Exemplo baixo:

```sql
UPDATE CARS
  SET color = 'white', year = 1970
  WHERE brand = 'Toyota';
```

Escreva
```sql
  SELECT * FROM cars;
```
Para ver as mudanças!
