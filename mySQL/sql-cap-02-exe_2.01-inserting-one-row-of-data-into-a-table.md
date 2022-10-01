# Exercise 2.01: Inserting One Row of Data into a Table

_Fonte: https://courses.packtpub.com/courses/take/sql/texts/9835434-exercise-2-01-inserting-one-row-of-data-into-a-table_



### Inserindo uma linha de dados em uma tabela



Neste exercício, implementaremos a instrução SQL INSERT INTO...VALUES para adicionar registros a uma tabela. Primeiro, criaremos um banco de dados EMPLOYEE e, em seguida, adicionaremos uma tabela a ele. Em seguida, inseriremos valores na tabela com a instrução INSERT SQL e, finalmente, exibiremos o conteúdo da tabela. Para isso, vamos seguir os seguintes passos:

'''javascript



'''

Crie um banco de dados **EMPLOYEE**:

```
CREATE DATABASE EMPLOYEE;
USE EMPLOYEE;
```

Crie uma tabela **departmentNo** como **PRIMARY KEY**:

```
CREATE TABLE department (
    departmentNo INT PRIMARY KEY,
    departmentName VARCHAR(20) NOT NULL,
    departmentLoc VARCHAR(50) NOT NULL
);
```

> Nota: A sintaxe utilizada será **PRIMARY KEY (departmentNo);**

Insira os valores na tabela **departament**:

```
INSERT INTO department (
    departmentNo,
    departmentName,
    departmentLoc
)
VALUES (
    1,
    'Engg',
    'Texas'
);
```

No painel Navegador, selecione a guia Esquemas. Selecione EMPREGADO | Tabelas | departamento | Selecione Linhas - Limite de 1000.
A saída esperada é a seguinte:

![img](https://files.cdn.thinkific.com/file_uploads/59347/images/5db/d94/f00/B14179_02_01.png)