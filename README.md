# Exercicio_BD
Primeiramente, abra o arquivo acima acima no SGBD PostgreSQL, usando a ferramenta PgAdmin4 no seu computador.

# 1ª Questão
Selecionar todos os dados dos países da tabela_paises

```
select * from tabela_paises;
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/9ff9b797-fc4f-4a5a-89d9-8bd99120548d)

# 2ª Questão
Selecione todas as cidades cujo país seja brazil

```
select cidade from tabela_paises
where pais = 'Brazil';
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/8c5ed8b4-73e2-48c9-9c93-166d9a00dc46)
# 3ª Questão
Selecione todas as cidades cuja região(estado) é ceará

```
select cidade from tabela_paises
where regiao = 'Ceará';
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/c20451a1-f7a4-4db4-889b-227342aca96b)

# 4ª Questão 
Utilize a função count para saber quantas regiões(estados) existem na China, utilize também o group by

```
select regiao, count (regiao)
from tabela_paises
where pais= 'China'
group by regiao;
```

# 5ª Questão
Quais regiões, diferentes, existem no Canadá?

```
select regiao, count (distinct regiao) 
from tabela_paises where pais= 'Canada! 
group by regiao;
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/ba631f84-d75e-46c7-85d7-be3902ede09c)

# 6ª Questão 
Quantos países diferentes existem na tabela 'tabela_paises';

```
select pais, count (distinct pais)
from tabela_paises
group by pais;
```

# 7ª Questão 
Quantas cidades diferentes existem no brazil;

```
select cidade, count (distinct cidade)
from tabela_paises
where pais= 'Canada'
group by cidade;
```
# 8ª Questão
Selecione os países e quantas regiões cada país possui

```
select pais, count (regiao) 
from tabela_paises
group by pais;
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/5304a62a-6cf6-4d3c-b58b-28076a57b4ac)

# 9ª Questão
Quantas pessoas com nome começando em 'João' existem no banco?

```
select nome
from tabela_paises
where nome like 'João%'
group by nome;
```

# 10ª Questão
Quantas pessoas têm o nome John?

```
select nome from tabela_paises
where nome like 'John%'
order by nome;
```

# 11ª Questão
Ordene os nomes dos países sem repetição em ordem alfabética;

```
select pais from tabela_paises
group by pais
order by pais asc;
```
![image](https://github.com/liviacarvalho07/Exercicio_BD/assets/111568402/f06f864d-7afd-47f7-a8a4-6443551cbf89)
