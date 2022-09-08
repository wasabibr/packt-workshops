# Exercício 1.02: Inserindo Valores na Tabela Clientes do Banco de Dados PACKT_ONLINE_SHOP
_Fonte: [https://courses.packtpub.com/courses/take/sql/texts/9835005-exercise-1-01-building-the-packt-online-shop-database](https://courses.packtpub.com/courses/take/sql/texts/9835006-exercise-1-02-inserting-values-into-the-customers-table-of-the-packt-online-shop-database)_

Agora que temos a tabela Customers pronta, vamos inserir valores na tabela usando uma única consulta. Temos os dados de uma planilha Excel já existente. Usaremos esses dados para escrever nossa consulta. Aqui está a aparência do arquivo do Excel:

>N.B.: Você pode encontrar o formato csv do arquivo neste endereço: [https://courses.packtpub.com/courses/take/sql/texts/9835006-exercise-1-02-inserting-values-into-the-customers-table-of-the-packt-online-shop-database](https://github.com/PacktWorkshops/The-SQL-Workshop/blob/master/Chapter01/Exercise%201.02.csv)

Para mover esses dados para o banco de dados, precisaremos executar as seguintes etapas:

1. Mudar para o banco de dados PACKT_ONLINE_SHOP:
```
USE PACKT_ONLINE_SHOP;
```

2. Insira os valores com base na planilha do Excel fornecida sempre que tivermos dados em branco. Usaremos NULL para fazer isso:
```
INSERT INTO Customers (FirstName, MiddleName, LastName, HomeAddress, Email, Phone,
Notes)
VALUES('Joe', 'Greg', 'Smith', '2356 Elm St.', 'joesmith@sfghwert.com', '(310)
555-1212', 'Always gets products home delivered'),
('Grace', 'Murray', 'Hopper', '123 Compilation Street', 'gmhopper@ftyuw46.com',
'(818) 555-3678', 'Compiler pioneer'),
('Ada', NULL, 'Lovelace', '22 Algorithm Way', 'adalovelace@fgjw54af.gov', '(717)
555-3457', 'First software engineer'),
('Joseph', 'Force', 'Crater', '1313 Mockingbird Lane', 'judgecrater@ev56gfwrty.com',
'(212) 555-5678', 'Works everyday'),
('Jacqueline', 'Jackie', 'Cochran', '1701 Flightspeed Avenue', 'jackiecochrane@
jryuwp8qe4w.gov', '(717) 555-3457', 'Researcher'),
(NULL, 'Paul', 'Jones', '126 Bonhomme Richard Ave.', 'jpjones@bonhommerichard.edu',
'(216) 555-6232', 'Admiral');
```

3. Ao executar a consulta e verificar o conteúdo da tabela Customers, você deverá ver a seguinte saída.


Com isso, você preencheu com sucesso a tabela Customers.
