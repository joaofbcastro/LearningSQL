# Agrupamentos

Nessa etapa aprendi sobre o método `GROUP BY` onde com ele podemos ter a contagem de items únicos de uma determinada coluna. 


Agregado a esse conhecimento, utilizei das lembranças do aprendizado anterior para fazer a contagem do total de clientes de cada sexo.

```sql
select 
	Sexo,
	count(*) as 'Qtd. Clientes'
from clientes
group by Sexo;
```

Aqui, como anteriormente, fiz a soma do total de produtos por marca.

```sql
select
	Marca_Produto,
	count(*) as 'Qtd. Produtos'
from produtos
group by Marca_Produto;
```

Partindo para uma tabela de pedidos, podemos ter uma noção do total de Receita e Custos fazendo a soma de todas as linhas das colunas Receita_Venda e Custo_Venda.

```sql
select
	ID_Loja,
	sum(Receita_Venda) as 'Receita Total',
	sum(Custo_Venda) as 'Custo Total'
from pedidos
group by ID_Loja;
```
