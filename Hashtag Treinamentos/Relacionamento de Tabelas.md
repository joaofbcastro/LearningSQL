# Relacionamento de tabelas

Nessa etapa, aprendi sobre relacionamento de tabelas com `INNER JOIN`.

Para isso foi precisso aprender sobre **chave primaria**, **chave estrangeira**, **tabela dimensão** e **tabela fato**.


## O que é uma chave estrangeira e uma chave primaria?

Uma chave primaria normalmente é um ID, algo que identifica uma linha, um valor único, ou seja, que não se repetirá durante toda a coluna.

Uma chave estrangeira é um ID que faz referência a uma outra linha de uma outra tabela. Sendo assim, poderá haver várias linhas com a mesma chave estrangeira.


## Tabela fato e tabela dimensão.

Uma **tabela dimensão** é uma tabela que contem as caracteristicas de um elemento. Ou seja, uma tabela que descreve o meu elemento.

Uma **tabela fato**, registrará acontecimentos em um determinado periodo de tempo. Por exemplo, vendas, devoluções, demissões, contratações. 

## Exemplo prático.

```sql
select
	l.Loja,
	l.Gerente,
	l.Telefone,
	sum(p.Receita_Venda) as Receita,
	sum(p.Custo_Venda) as Custos,
	sum(p.Qtd_Vendida) as Qtd_Vendida
from pedidos p
inner join lojas l 
	on p.ID_Loja = l.ID_Loja
group by l.Loja;
```
