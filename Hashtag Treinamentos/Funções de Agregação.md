# Funções de agregação

Como em toda situação de nossas vidas, hora ou outra necessitaremos de realizar calculos ao utilizar o SQL, nessa etapa de meu aprendizado desenvolvi afinidade com algumas funlões de agregação do SQL.

O `CUNT([COLUNA])` é utilizado para contar o total de linhas de uma coluna.
```sql
SELECT count(Nome)
FROM clientes;
```

O `COUNT(*)` é utilizado para contar o total de linhas de uma tabela.
```sql
SELECT count(*)
FROM clientes;
```

O `COUNT(DISTINCT [COLUNA])` serve para contar os valores distintos dentro de uma coluna.
```sql
SELECT COUNT(DISTINCT Escolaridade)
FROM clientes;
```

O `SUM([COLUNA])` faz a soma de todos os valores de uma coluna.
```sql
SELECT SUM(Renda_Anual)
FROM clientes;
```

O `AVG([COLUNA])` faz a média de todos os valores de uma coluna.
```sql
SELECT AVG(Receita_Venda)
FROM pedidos;
```

O `MIN([COLUNA])` mostra o valor mínimo dentro de uma coluna.

```sql
SELECT MIN(Receita_Venda)
FROM pedidos;
```

O `MAX([COLUNA])` mostra o valor máximo dentro de uma coluna.
```sql
SELECT MAX(Receita_Venda)
FROM pedidos;
```
