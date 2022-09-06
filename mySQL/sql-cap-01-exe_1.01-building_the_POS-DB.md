# Exercise 1.01: Building the PACKT_ONLINE_SHOP Database

_Fonte: https://courses.packtpub.com/courses/take/sql/texts/9835005-exercise-1-01-building-the-packt-online-shop-database_


## Construindo o banco de dados PACKT_ONLINE_SHOP

> Neste exercício, vamos começar a construir o banco de dados para uma loja online da Packt — uma loja que vende uma variedade de itens aos clientes. A Packt Online Shop tem trabalhado em planilhas até agora, mas como planejam aumentar a escala, percebem que essa não é uma opção viável e, portanto, desejam avançar para o gerenciamento de dados por meio do SQL. O primeiro passo neste processo será criar um banco de dados chamado PACKT_ONLINE_SHOP com uma tabela para armazenar os detalhes de seus clientes. 

Execute as seguintes etapas para concluir este exercício:

1. Criar um banco de dados usando a instrução **create**
```
create database PACKT_ONLINE_SHOP;
```

2. Mudar para este banco de dados
```
use PACKT_ONLINE_SHOP;
```

3. Crie a tabela **Customers**
```
create table Customers
(
    FirstName varchar(50) ,
    MiddleName varchar(50) ,
    LastName varchar(50) ,
    HomeAddress varchar(250) ,
    Email varchar(200) ,
    Phone varchar(50) ,
    Notes varchar(250)
);
```

**N.B.:** *Nota: Semelhante a **varchar**, **nvarchar** é um tipo de dados de comprimento variável; no entanto, em nvarchar, os dados são armazenados em Unicode, não em ASCII. Portanto, as colunas definidas com nvarchar também podem conter valores em outras linguagens. nvarchar requer 2 bytes por caractere, enquanto varchar usa 1 byte.*

4. Execute a instrução clicando no botão executar
```
nnn
```

5. Revise a tabela clicando com o botão direito do mouse na tabela na **Schemas tab** e clicando em **Select Rows - Limit 1000** no menu contextual
```
nnn
```
Isso executa uma consulta **Select** simples. Você aprenderá sobre a instrução **Select** no Capítulo 4, a instrução **SELECT**. As primeiras 1.000 linhas são exibidas. Como ainda não inserimos valores na tabela, só podemos visualizar os cabeçalhos das colunas na **Result Grid**.

**N.B.:** *se você estiver trabalhando no Microsoft SQL Server, poderá fazer isso clicando com o botão direito do mouse na tabela na janela do Pesquisador de objetos e selecionando **Select Top 1000 Rows**.*

Na próxima seção, veremos como inserir valores em tabelas.
