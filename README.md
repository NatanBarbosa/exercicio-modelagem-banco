# Conceitualização do banco de dados de uma seguradora 

## Enunciado
Uma seguradora para carros Mario & Luigi está trabalhando com alta demanda de serviços e precisa se modernizar para poder crescer com qualidade. A empresa não possui um banco de dados completo e faz diversas anotações em papel ou em Excel o que prejudica muito o gerenciamento das equipes, das receitas e dos recursos. 

Como contratados vocês devem oferecer a eles uma solução digital de um banco e primeiro passo para isso é o planejamento desses dados: o que eles devem fazer? Como devem fazer? Quais são as principais informações? 

Vamos elaborar um diagrama para uma seguradora de automóveis:
Entidades: Cliente, Apólice, Carro e Acidentes.

## Processo de resolução do problema
Cada tabela e coluna foi pensada e estruturada no modelo de banco relacional MySql, considerando chaves primárias e estrangeiras para ligação entre tabelas.
O modelo conceitual das tabelas está no arquivo [Modelo conceitual do banco de dados](Atividade Mario&Luigi.pdf)

### Tabela cliente
O cliente da seguradora terá um identificador, nome e informações de endereço. O cliente da seguradora terá conexões com outras tabelas do modelo, e essas informações nas colunas são muito importantes para identificá-lo

### Tabela carro
O carro terá um identificador, marca e modelo para ser reconhecido.
Um cliente pode ter vários carros pertencentes à ele nessa seguradora.

### Tabela apolice e tipos_apolice
A apólice é o contrato que garantirá que a seguradora aceite os riscos por parte dela e dará cobertura para o cliente conforme definido no contrato.
Pensando nisso, na tabela apólice é necessário definir o valor mensal que o cliente pagará, as cláusulas do documento, a que cliente e a que carro essa apólice está direcionada
Cada apólice dá cobertura a somente um carro, ou seja, um carro estará relacionado à apenas uma apólice
Além disso, uma apólice está relacionada à algum tipo de apólice.

### Tabela acidente
Nessa tabela será registrado algumas informações do acidente que um determinando carro se envolveu
Para isso, nessa tabela tem-se o identificador do acidente, a data e hora e o local que o acidente ocorreu, a descrição dele, se ele foi coberto ou não (enquanto esse campo for nulo, ainda está sendo decidido) e o identificador do carro que se envolveu nesse acidente.
