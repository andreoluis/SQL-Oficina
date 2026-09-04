# SQL-Oficina

🛠️ Apresentação — Banco de Dados de uma Oficina Mecânica
📌 Sobre o projeto

Este projeto consiste no desenvolvimento de um banco de dados para organizar e gerenciar as informações de uma oficina mecânica.

A escolha desse tema ocorreu porque uma oficina trabalha diariamente com diversos tipos de dados, como:

👥 Clientes;
🚗 Veículos;
🔧 Mecânicos;
🛠️ Serviços;
📋 Ordens de serviço;
💰 Valores e atendimentos realizados.

O principal objetivo foi criar uma estrutura organizada que facilitasse o cadastro, o relacionamento e a consulta dessas informações.

🗂️ Estrutura do banco de dados

O banco de dados é composto por seis tabelas principais:

clientes
veiculos
mecanicos
servicos
ordens_servico
itens_ordem_servico
👥 clientes

Armazena os dados dos clientes da oficina, como nome, telefone, e-mail e cidade.

🚗 veiculos

Guarda as informações dos veículos cadastrados. Essa tabela possui uma chave estrangeira que relaciona cada veículo ao seu respectivo proprietário.

🔧 mecanicos

Contém os dados dos funcionários da oficina e suas especialidades.

🛠️ servicos

Armazena os serviços oferecidos pela oficina e seus respectivos valores.

📋 ordens_servico

Registra os atendimentos realizados. Nessa tabela são armazenadas informações como:

Veículo atendido;
Mecânico responsável;
Data de entrada;
Data de saída;
Status do serviço.
🧾 itens_ordem_servico

Foi criada porque uma única ordem de serviço pode conter vários serviços.

Essa tabela realiza a ligação entre as ordens de serviço e os serviços executados em cada atendimento.

🔗 Relacionamento entre as tabelas

A estrutura do banco segue a seguinte lógica:

CLIENTE
   │
   └── possui
          │
          ▼
       VEÍCULO
          │
          └── recebe
                 │
                 ▼
          ORDEM DE SERVIÇO
             │          │
             │          └── é realizada por
             ▼                         │
          SERVIÇOS ◄──── MECÂNICO

Uma ordem de serviço pode conter um ou mais serviços, por isso a tabela itens_ordem_servico é utilizada para representar esse relacionamento.

🔑 Chaves utilizadas

Para organizar os relacionamentos entre as tabelas, foram utilizadas:

Primary Key

As Primary Keys identificam cada registro de forma única dentro de uma tabela.

Foreign Key

As Foreign Keys permitem relacionar os dados entre diferentes tabelas.

Por exemplo, a tabela veiculos possui uma chave estrangeira que indica a qual cliente cada veículo pertence.

🧱 Tipos de dados utilizados

Foram utilizados diferentes tipos de dados de acordo com cada informação:

Tipo de dado	Utilização
INTEGER	Anos, identificadores e quantidades
DATE	Datas de entrada e saída
TEXT	Nomes, placas, cidades e outras informações textuais
NUMERIC	Valores monetários dos serviços
🔎 Pesquisa realizada

Como parte da pesquisa solicitada no trabalho, foi utilizada a Tabela FIPE para consultar informações sobre veículos, como:

Marcas;
Modelos;
Anos de fabricação;
Valores de referência.

Essas informações ajudaram a tornar os dados cadastrados mais próximos de uma situação real.

💻 Consultas SQL realizadas

No Supabase, foram realizadas consultas utilizando comandos SQL como:

SELECT — para consultar informações;
WHERE — para filtrar resultados;
ORDER BY — para organizar os dados;
JOIN — para relacionar informações de diferentes tabelas;
SUM — para calcular o valor total dos serviços.

Com essas consultas, foi possível demonstrar que o banco de dados consegue:

Pesquisar informações;
Filtrar resultados;
Organizar registros;
Relacionar dados de diferentes tabelas;
Calcular valores totais dos serviços realizados.
✅ Conclusão

O projeto apresenta um banco de dados organizado para o gerenciamento de uma oficina mecânica.

A estrutura criada permite controlar clientes, veículos, mecânicos, serviços e ordens de serviço de forma relacionada e eficiente.

Além disso, as consultas SQL demonstram como os dados podem ser pesquisados, filtrados, organizados e utilizados para gerar informações importantes para o funcionamento da oficina.
