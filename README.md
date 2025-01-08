# Projeto_modelagem_E-COMMERCE

Modelagem de Banco de Dados para E-commerce

Descrição do Projeto

Este projeto apresenta uma modelagem de banco de dados relacional para um sistema de e-commerce. O modelo foi criado com o objetivo de gerenciar informações sobre clientes, produtos, pedidos, pagamentos e entregas de forma eficiente, garantindo a integridade dos dados e facilitando operações e análises relacionadas ao negócio.

A modelagem foi realizada utilizando o MySQL Workbench, com foco em boas práticas de estruturação e normalização, atendendo aos principais requisitos funcionais de um sistema de e-commerce.

Entidades Principais e Relacionamentos

1. Cliente
Dados: Nome, CPF/CNPJ, Contato, Endereço, E-mail, Data de Cadastro.
Relacionamento: Um cliente pode realizar múltiplos pedidos.

2. Produto
Dados: Nome, Descrição, Preço, Quantidade em Estoque, Categoria.
Relacionamento: Cada produto pertence a uma categoria, e pode estar relacionado a múltiplos pedidos.

3. Categoria
Dados: Nome da Categoria.
Relacionamento: Cada categoria pode ter vários produtos associados.

4. Pedido
Dados: Data do Pedido, Valor Total, Status do Pedido.
Relacionamento: Um pedido é feito por um cliente e pode conter múltiplos produtos.

5. ItemPedido
Dados: Quantidade, Preço Unitário.
Relacionamento: Representa os produtos associados a um pedido.

6. Pagamento
Dados: Método de Pagamento, Status do Pagamento, Data do Pagamento.
Relacionamento: Um pagamento está associado a um pedido.

7. Entrega
Dados: Transportadora, Código de Rastreamento, Datas de Envio e Entrega.
Relacionamento: Está associada a um pedido específico.

Características Técnicas

Relacionamentos implementados com chaves estrangeiras para garantir integridade referencial.
Uso do tipo ENUM no campo Status da tabela Pedido para padronizar valores (ex.: "Pendente", "Pago", "Cancelado").
Definição de tipos de dados adequados para valores monetários (DECIMAL(10,2)) e chaves primárias (INT).
Como Utilizar

1. Clone o Repositório

Copiar código
git clone https://github.com/seuusuario/nome-do-repositorio.git

2. Importe o Arquivo SQL
Abra o MySQL Workbench e importe o arquivo SQL com a estrutura do banco de dados para recriar o modelo.

3. Use o Banco de Dados
Utilize o banco para testes, simulações ou como base para desenvolvimento de sistemas de e-commerce.

Tecnologias Utilizadas

Ferramenta de Modelagem: MySQL Workbench
Banco de Dados Relacional: MySQL

Possíveis Melhorias Futuras

Implementação de logs para auditoria de transações.
Adicionar tabelas para cupons de desconto e devoluções.
Automatização de cálculos como o valor total do pedido com triggers.
