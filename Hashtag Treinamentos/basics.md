# Práticas básicas sobre consultas em SQL.

Para a execução dessas queries utilizei o DBeaver e o banco de dados foi um banco MySQL construido e disponibilizado pelo pessoal da Hashtag Treinamentos.


Selecionando apenas os produtos da marca DELL ou SAMSUNG, porém, mudando o nome de exibição das colunas. 
```sql
select 
	ID_Produto as 'ID do Produto',
	Nome_Produto as 'Nome do Produto',
	Preco_Unit as 'Preço Unitário' 
from produtos 
where Marca_Produto = 'DELL' or Marca_Produto  = 'SAMSUNG';
```

Selecionando todos os produtos que possuem o preço maior ou igual a R$ 1.800,00.
````sql
select * from produtos
where Preco_Unit >= 1800;
````

Selecionando apenas os produtos com preços iguais a R$ 3.100,00.
````sql
select * from produtos
where Preco_Unit = 3100;
````

Selecionando apenas os produtos da marca DELL.
````sql
select * from produtos
where Marca_Produto = 'DELL';
````

Selecionando apenas os pedidos feitos no dia 03/01/2019.
````sql
select * from pedidos
where Data_Venda = '2019-01-03';
````

Selecionando apenas os clientes com estado civil declarado como solteiro e do sexo masculino.
````sql
select * from clientes
where Estado_Civil = 'S' and Sexo = 'M';
````

Selecionando apenas os produtos da marca DELL ou SAMSUNG.
````sql
select * from produtos
where Marca_Produto = 'DELL' or Marca_Produto = 'SAMSUNG';
````

