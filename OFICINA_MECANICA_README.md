Projeto de Esquema Conceitual de Oficina Mecânica
## Título do Repositório: esquema-conceitual-oficina-mecanica

## Descrição:

Este repositório contém o esquema conceitual desenvolvido para um sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica. O esquema foi criado com base na narrativa fornecida e visa modelar as entidades, atributos e relacionamentos envolvidos no processo de manutenção de veículos.

## Contexto:

O sistema tem como objetivo gerenciar o fluxo de trabalho em uma oficina mecânica, desde a criação de uma ordem de serviço (OS) até a conclusão dos serviços e a geração da fatura. As principais funcionalidades do sistema incluem:

Cadastro de clientes e veículos: Permite registrar os dados dos clientes e dos veículos que serão atendidos.
Criação de ordens de serviço: Facilita a criação de novas ordens de serviço, com informações detalhadas sobre os serviços a serem realizados.
Gerenciamento de equipes: Permite cadastrar os mecânicos e suas especialidades, além de atribuir as ordens de serviço às equipes.
Cálculo de custos: Realiza o cálculo do valor total de cada ordem de serviço, considerando a mão de obra e as peças utilizadas.
Gerenciamento do status das ordens de serviço: Permite acompanhar o andamento das ordens de serviço, desde a criação até a conclusão.
## Esquema Conceitual:

![images](https://github.com/Eudesjs/Projeto_Suzano_An-lise_De_Dados_BI/blob/21d55e1d5c5a6a6effff99fe102609f431bb869d/Projeto_E-Commerce_DIO.png)

## Entidades e Atributos:

Cliente: código, nome, endereço, telefone
Veículo: chassi, modelo, ano, placa, cliente (relacionamento)
Mecânico: código, nome, endereço, especialidade
Ordem de Serviço (OS): número, data_emissão, valor_total, status, data_conclusão, veículo (relacionamento), equipe (relacionamento)
Serviço: descrição, valor_hora, peça (relacionamento)
Peça: código, descrição, valor_unitário
Equipe: código, nome, mecânicos (relacionamento)
## Relacionamentos:

Um cliente pode ter vários veículos.
Um veículo está associado a uma única ordem de serviço.
Uma ordem de serviço pode ter vários serviços.
Um serviço pode necessitar de várias peças.
Uma equipe é composta por vários mecânicos.
Uma ordem de serviço é atribuída a uma única equipe.
## Considerações:

Tabela de referência de mão-de-obra: Não foi detalhado na narrativa como essa tabela será utilizada. Assumiu-se que ela conterá informações sobre o valor por hora de cada tipo de serviço.
Autorização do cliente: Não foi especificado como o sistema irá registrar a autorização do cliente para a execução dos serviços.
Histórico de serviços: Poderá ser interessante adicionar uma entidade para registrar o histórico de serviços realizados em cada veículo.
