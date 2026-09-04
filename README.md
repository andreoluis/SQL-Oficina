# SQL-Oficina

Este projeto consiste em um banco de dados desenvolvido para organizar as informações de uma oficina mecânica.

Escolhi esse tema porque uma oficina trabalha com vários tipos de dados no dia a dia, como clientes, veículos, mecânicos, serviços e ordens de serviço. A ideia foi criar uma estrutura que facilitasse o cadastro e a consulta dessas informações.

O banco de dados possui seis tabelas principais:

clientes
veiculos
mecanicos
servicos
ordens_servico
itens_ordem_servico

A tabela clientes armazena os dados dos clientes da oficina. A tabela veiculos guarda as informações dos veículos e possui uma chave estrangeira que relaciona cada veículo ao seu proprietário.

A tabela mecanicos contém os dados dos funcionários e suas especialidades. Já a tabela servicos armazena os serviços oferecidos pela oficina e seus respectivos valores.

A tabela ordens_servico registra os atendimentos realizados. Nela ficam armazenadas informações como o veículo atendido, o mecânico responsável, a data de entrada, a data de saída e o status do serviço.

Também criei a tabela itens_ordem_servico, pois uma ordem de serviço pode ter mais de um serviço. Essa tabela faz a ligação entre as ordens de serviço e os serviços realizados em cada atendimento.

Para organizar os relacionamentos entre as tabelas, utilizei Primary Keys e Foreign Keys. As Primary Keys identificam cada registro de forma única, enquanto as Foreign Keys permitem relacionar os dados entre as tabelas.

Também utilizei diferentes tipos de dados de acordo com cada informação. Por exemplo:

INTEGER para anos e quantidades;
DATE para datas;
TEXT para nomes e outras informações textuais;
NUMERIC para valores monetários.

Como parte da pesquisa solicitada no trabalho, utilizei a Tabela FIPE para consultar informações sobre veículos, como marcas, modelos e anos.

No Supabase, realizei algumas consultas SQL utilizando comandos como SELECT, WHERE, ORDER BY e JOIN. Também utilizei funções como SUM para calcular valores totais dos serviços.

Com essas consultas, foi possível demonstrar que o banco consegue pesquisar informações, filtrar resultados, organizar os dados e relacionar informações de diferentes tabelas.
