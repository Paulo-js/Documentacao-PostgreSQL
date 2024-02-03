# Como adicionar colunas em uma tabela já existente 

## Índice:
- Para que serve a declaração `ALTER TABLE`.
- Como usar a declaração `ALTER TABLE`.
- Certificar se tudo deu certo.

---
---

## Para que serve a declaração `ALTER TABLE`.

- Adicionar uma coluna à uma tabela existente.
- Para adicionar, deletar ou modificar colunas em uma tabela existente.
- Usada para adicionar e descartar várias restrições em uma tabela existente.

## Como usar a declaração `ALTER TABLE`

Por enquanto, usaremos a declaração `ALTER TABLE` para **adicionar** uma coluna chamada *color* na nossa tabela existente *cars*.

- Para fazer isso, é necessário especificar qual tabela queremos modificar.
  
- Especificar o tipo de dado que queremos adicionar. No caso o dado vai ser do tipo *string*, ou seja, do tipo texto. Para isso, é necessário usar a palavra-chave: `VARCHAR` e então dizer quantos caracteres são permitidos pra aquela string.

- Para sinalizar ao nosso banco de dados que queremos **adicionar** uma coluna à nossa tabela, é usado o comando `ADD`.

Exemplo abaixo:

```sql
ALTER TABLE cars
ADD color VARCHAR(255);
```

O que irá retornar o seguinte:

```
ALTER TABLE
```


---

## Certificar se tudo deu certo

Para certificar se deu tudo certo, mostre todos os dados da tabela usando o a declaração `SELECT`.

Exemplo abaixo:

```sql
SELECT * FROM cars;
```

Você verá que foi adicionado uma coluna vazia chamada *color* à nossa tabela *cars*.

Resultado:

````
| brand  | model  | year | color  
| ------ + ------ + ---- + ------
| Volvo  | p1800  | 1968 |
| BMW    | M1     | 1978 |
| Toyota | Celica | 1975 |
(4 registros)
