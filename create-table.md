# Inserir dados no banco de dados PostgreSQL

## Índice: 
- O que é `CREATE TABLE` e para o que serve.
- Explicando o que foi feito.
- Como mostrar os dados da tabela vazia criada aqui.


## Query: `CREATE TABLE`

A declaração `CREATE TABLE` é usada para criar tabelas no Banco de dados PostgreSQL:

```sql
  CREATE TABLE cars (
    brand VARCHAR(255),
    model VARCHAR(255),
    year INT
  );
```

Quando a declaração acima for executada, uma tabela chamada *cars* irá ser criada, e o Shell irá retornar o seguinte: 

```
CREATE TABLE
```

No Shell no seu computador, depois que você fizer tudo isso, o Shell no seu computador deve **VISUALMENTE** parecer com isso:

```
CREATE TABLE cars (
  brand VARCHAR(255),
  model VARCHAR(255),
  year INT
);
CREATE TABLE
```

---

## Explicando tudo que feito até agora

A Declaração SQL usada acima (`CREATE TABLE`) criou uma tabela com três campos: `brand`, `model`, and `year`.

Quando criada uma tabela, devemos especificar os tipos de dados de cada campo. 

Para os campos `brand` e `model` foi usado dois valores de *string*, que foram específicados através da palavra-chave `VARCHAR`.

É necessário expecificar o número de caractéres permitidos no campo de *string*, no caso foi especificado que o limite seria 255.

Para o campo `year` foi integrado um dado do tipo *inteiro* (número sem decimais), com o a palavra-chave `INT`.

---

## Mostrando dados da tabela

Para mostrar os dados da tabela vazia criada a pouco, deve-se usar outra declaração do SQL:

```
SELECT * FROM cars;
```

Que irá resultar nisto:

```

| brand | model | year |
| ------+-------+----- |
(0 rows)

