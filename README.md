Laboratório de Banco de Dados (MySQL) - IESB

Repositório destinado à resolução da Verificação de Aprendizagem da disciplina de Laboratório de Banco de Dados do Centro Universitário IESB. O projeto consiste na criação, inserção e consulta de dados em um ambiente relacional simulando um departamento de contas a receber.

Tecnologias Utilizadas

Banco de Dados: MySQL

Ferramenta de Gestão: MySQL Workbench

Linguagem: SQL (DDL e DML)

Estrutura do Projeto

O script completo com a criação da tabela, inserção de dados e todas as queries executadas está disponível no arquivo banco_de_dados.sql.

Resolução das Atividades

Abaixo estão detalhadas as explicações de cada query solicitada no exercício, juntamente com as evidências (prints) da execução no MySQL Workbench.

1. Criação da Tabela e Inserção de Dados

Explicação: Foi criada a tabela duplicata definindo os tipos de dados adequados (como DATE para datas e DECIMAL para valores monetários), sendo a coluna Numero definida como PRIMARY KEY. Em seguida, realizou-se a inserção (INSERT INTO) dos registros iniciais em letras maiúsculas.


Questão 1: Listar nome, vencimento e valor de cada duplicata.

Explicação: Utilizamos o comando SELECT focado especificamente nas colunas requisitadas, ignorando as demais, para otimizar a visualização.


Questão 2: Apresentar o número das duplicatas depositadas no banco Itaú.

Explicação: A cláusula WHERE foi aplicada ao campo Banco para filtrar apenas as linhas cujo valor exato correspondesse à string 'ITAU'.


Questão 3: Quais são as duplicatas que vencem no ano de 2017.

Explicação: Para esta filtragem, a função YEAR() nativa do MySQL foi utilizada na coluna Vencimento para extrair apenas o ano da data e compará-lo com 2017.


Questão 4: Duplicatas não depositadas nos bancos Itaú e Santander.

Explicação: A condição NOT IN foi empregada para excluir, em uma única instrução, os registros cujos bancos correspondessem aos valores da lista ('ITAU', 'SANTANDER').


Questão 5: Valor da dívida do cliente PAPELARIA SILVA e suas duplicatas.

Explicação: Foram executadas duas ações: a primeira, um SELECT simples para listar as duplicatas individuais do cliente. A segunda, utilizando a função de agregação SUM(Valor), somou todas as dívidas criando uma coluna virtual (AS Valor_Total_Divida) para exibir o resultado consolidado.


Questão 6: Retirar da tabela a duplicata 770710 (LIVRARIA FERNANDES).

Explicação: A instrução DELETE FROM removeu o registro permanentemente da base. A exclusão foi feita de forma segura utilizando a chave primária (Numero = 770710) para garantir que nenhuma outra linha fosse afetada.


Questão 7: Listagem de todos os campos em ordem alfabética pelo nome.

Explicação: O comando SELECT * buscou todas as colunas da tabela, enquanto a cláusula ORDER BY Nome ASC organizou os resultados de forma ascendente (alfabética) baseada na coluna Nome.


Questão 8: Listagem ordenada por data de vencimento (nome, banco, valor e vencimento).

Explicação: Foi feita uma seleção restrita das colunas solicitadas, e os dados foram ordenados do mais antigo para o mais recente utilizando ORDER BY Vencimento ASC.


Projeto desenvolvido para fins acadêmicos.
