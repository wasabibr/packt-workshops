# Capítulo 2 - Manipulando Dados
_nnn_


## Visão geral

Este capítulo ensina você a implementar as instruções INSERT, UPDATE e DELETE que ajudam a manter o conteúdo presente em uma tabela atualizado. Também abordaremos como podemos usar valores padrão ao atualizar as tabelas.

## Introdução

No Capítulo 1, Noções básicas de SQL, aprendemos os conceitos que ajudam a configurar um banco de dados. Embora tenhamos inserido alguns dados nas tabelas, não entramos nos detalhes do gerenciamento dos dados no banco de dados. No entanto, pode haver circunstâncias em que possamos precisar alterar os dados inseridos ou presentes no banco de dados. Por exemplo, um funcionário que trabalha para uma empresa pode querer alterar seu número oficial do que foi atualizado anteriormente. Um produto que não é mais fabricado precisa ser removido da lista de produtos disponíveis. O MySQL fornece alguns comandos que podemos implementar para fazer alterações no banco de dados, que serão abordados neste capítulo. Neste capítulo, preencheremos as tabelas que criamos no capítulo anterior com dados. Também veremos as operações UPDATE e DELETE que fazem parte do CRUD.

## A operação INSERIR

A operação INSERT insere um registro em uma tabela. Já usamos a operação de inserção no capítulo anterior, no entanto, neste capítulo, estamos analisando-a com mais detalhes. A seguir estão alguns pontos importantes sobre a operação INSERT:

- Nem sempre é essencial fornecer dados para cada coluna ao executar uma operação INSERT. As colunas podem ser deixadas em branco, a menos que haja uma restrição que proíba isso. Algumas colunas podem até ter valores padrão ou gerados pelo sistema.
- Você não deve alterar os valores gerados pelo sistema.
- Os valores da coluna devem corresponder aos requisitos de ordem, tipo de dados e tamanho.
- Os valores a serem inseridos na tabela devem estar entre aspas no caso de strings, data-hora e caracteres. Os números não devem ser colocados entre aspas.
- Se você não especificar os nomes das colunas na instrução INSERT, seu registro deverá ter um valor para todas as colunas. Além disso, você deve manter a sequência de colunas nos valores.
- Você só pode inserir valores em uma tabela por vez porque INSERT INTO aceita apenas um nome de tabela como argumento de nome de tabela.

### Executando um simples INSERT

Como vimos anteriormente, a instrução INSERT começa com INSERT INTO, seguida do nome da tabela. Em seguida, você especifica os nomes das colunas. É obrigatório inserir dados em todas as colunas que requerem informações (por exemplo, colunas especificadas como NOT NULL ou uma coluna selecionada como chave primária).

Colunas em branco não precisam ser fornecidas com dados usando a instrução INSERT. Além disso, pode haver colunas com valores padrão; estes também não precisam ser fornecidos com dados, a menos que seja necessário.

Depois de especificar os nomes das colunas, você pode usar a cláusula VALUES para inserir os valores dessas colunas. Em outras palavras, você não pode especificar o nome de uma coluna e não fornecer dados a ela. Se você não deseja inserir dados em uma coluna, não especifique o nome da coluna na instrução INSERT INTO.

Este processo é tão simples quanto parece. Dessa forma, você insere uma linha ou registro na tabela. No entanto, em muitos casos, é recomendável usar a operação UPDATE junto com a palavra-chave SET para inserir linhas, pois o processo é mais eficiente.

>Nota: Discutiremos a operação UPDATE e seu uso com a palavra-chave SET em detalhes na seção Operação UPDATE neste capítulo.