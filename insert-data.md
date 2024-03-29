# Inserir dados no banco de dados PostgreSQL

## índice:
- Inserir dados em tabelas.
- Explicando as declarações SQL usadas.
- Mostrando os dados na tabela.
- Inserção de múltiplos registros.

---
---

# Inserir dados em tabelas

É necessário usar a declaração `INSERT INTO`.

A seguinte declaração irá inserir dados na tabela chamada *cars*.

```sql
INSERT INTO cars (brand, model, year)
VALUES ('Ford', 'Mustang', 1964);
```

O Shell irá retornar o seguinte:

```
INSERT 0 1
```

Que significa que o registro 1 foi inserido.

**IMPORTANTE:** Ignore o `0` por enquanto, só saiba que ele representa algo que sempre será `0`.

# Mostrando os dados da tabela

É usado o seguinte comando para verificar se os dados foram inseridos corretamente:

```sql
SELECT * FROM cars;
```

Que irá retornar o seguinte:

| brand | model   | year |
| ----- | ------- | ---- |
| Ford  | Mustang | 1964 |


# Explicações sobre as declarações SQL usadas

Perceba que na declaração SQL usada acima (`INSERT INTO`), os valores de *string* (*texto*) devem ser escrito com aspas simples.

Valores numéricos podem ser escritos sem aspas simples, mas podem ser incluídas se quiser.

# Inserção de múltiplos registros

Para inserir múltiplos registros de dados, é usada a mesma declaração (`INSERT INTO`), mas com múltiplos valores. <br>

Exemplo abaixo:

```sql
INSERT INTO cars(brand, model, year)
VALUES
  ('Volvo', 'p1800', 1968),
  ('BMW', 'M1', 1978),
  ('Toyota', 'Celica', 1975);
```

o Shell irá retornar o seguinte:

```
INSERT 0 3
```

Significa que `3` registros foram inseridos com sucesso.

## Para se certificar que tudo funcionou como deveria, mostre os dados da tabela.

```sql
SELECT * FROM cars;
```

O que irá retornar o seguinte:

| brand  | model  | year |
| ------ | ------ | ---- |
| Volvo  | p1800  | 1968 |
| BMW    | M1     | 1978 |
| Toyota | Celica | 1975 |
