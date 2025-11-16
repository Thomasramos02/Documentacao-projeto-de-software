📘 Projeto de Software – Sistema de E-Commerce de Suplementos

Este repositório apresenta a modelagem completa de um sistema de e-commerce de suplementos, desenvolvido para a disciplina Projeto de Software.
Inclui todos os artefatos exigidos no processo de análise e design, seguindo padrões UML.

📑 Sumário

Descrição Geral

Escopo do Sistema

Casos de Uso

Diagramas UML

Diagrama de Casos de Uso

Diagrama de Classes

Diagramas de Sequência

Diagramas de Comunicação

Diagramas de Estados

Diagramas de Componentes

Diagrama de Implantação

Modelo de Dados (DER)

Estratégias de Mapeamento Objeto–Relacional

Tecnologias Sugeridas

Autores

🧾 Descrição Geral

O sistema modelado representa um e-commerce de suplementos, permitindo que clientes realizem compras online, acompanhem pedidos e gerenciem suas contas.
Administradores podem controlar produtos, usuários e pedidos.

A modelagem segue os princípios de análise orientada a objetos, utilizando UML como linguagem padrão.

🎯 Escopo do Sistema

O sistema oferece suporte às seguintes funcionalidades:

👤 Cliente

Criar conta

Editar/Excluir conta

Realizar compras

Acompanhar status dos pedidos

🛠️ Administrador

Gerenciar produtos

Gerenciar pedidos

Gerenciar usuários

📁 Casos de Uso

A seguir, os principais casos de uso definidos:

ID	Caso de Uso	Atores	Descrição
UC-01	Finalizar Compra	Cliente	Concluir a compra de suplementos.
UC-02	Acompanhar Pedido	Cliente	Ver o andamento e status da entrega.
UC-03	Gerenciar Conta	Cliente/Admin	Agrupa criação, edição e exclusão de conta.
UC-03.1	Criar Conta	Usuário	Criar uma nova conta.
UC-03.2	Editar Conta	Usuário	Editar dados pessoais.
UC-03.3	Excluir Conta	Usuário	Remover conta definitivamente.
UC-04	Gerenciar Pedidos	Admin	Alterar status, cancelar e visualizar pedidos.
UC-05	Gerenciar Produtos	Admin	Incluir, remover e editar produtos.
🧩 Diagramas UML

A seguir, a lista dos diagramas produzidos no exercício.

📌 Diagrama de Casos de Uso

Representa as interações entre usuários e funcionalidades do sistema.

(Diagramas incluídos no repositório em /diagrams/usecase/)

📌 Diagrama de Classes

Modelo estrutural com associações, atributos e operações relevantes.

(Gerado com PlantUML — incluído em /diagrams/class/)

📌 Diagramas de Sequência

Diagramas criados:

Cliente finaliza compra

Cliente faz login

Admin gerencia produtos

Admin administra usuários

Cliente acompanha pedido

Cada um mostra o fluxo temporal das mensagens entre objetos.

(Disponíveis em /diagrams/sequence/)

📌 Diagramas de Comunicação

Todos os fluxos:

Cliente faz pedido

Cliente faz login

Admin gerencia usuários

(Código PlantUML disponível em /diagrams/communication/)

📌 Diagramas de Estados

Estados principais de:

Pedido (Criado → Pago → Enviado → Entregue / Cancelado)

Conta de usuário

(Arquivos em /diagrams/state/)

📌 Diagrama de Componentes

Mostra a organização dos módulos lógicos:

Frontend Web

API Backend (Controllers + Services + Repositories)

Banco de Dados

(Arquivo em /diagrams/component/)

📌 Diagrama de Implantação

Mostra onde o sistema é executado:

Servidor Frontend (Navegador)

Servidor Backend

Banco de Dados

(Arquivo em /diagrams/deployment/)

📌 Modelo de Dados (DER – PlantUML)

Inclui:

Usuário

Produto

Pedido

Item_Pedido

Pagamento

Com todos os relacionamentos e cardinalidades.

(Arquivo em /diagrams/database/modelo_dados.puml)

🔄 Estratégias de Mapeamento Objeto–Relacional
Classe	Tabela	Mapeamento
Usuario	usuario	1:1 direto
Produto	produto	1:1 direto
Pedido	pedido	FK para usuário
ItemPedido	item_pedido	Tabela associativa Pedido × Produto
Pagamento	pagamento	1:1 com Pedido

Padrões aplicados:

FK para representar associações 1:N

Tabela intermediária para composição de itens

Enum para tipo de usuário

Normalização 3FN

🛠️ Tecnologias Sugeridas

Embora o projeto seja de modelagem, uma implementação possível incluiria:

Backend: Node.js, Spring Boot ou Laravel

Frontend: React, HTML/CSS/Bootstrap

Banco: PostgreSQL ou MySQL

UML: PlantUML + Draw.io

👨‍💻 Autor

Thomas Ramos
PUC Minas — Engenharia de Software
Disciplina: Projeto de Software# Documentacao-projeto-de-software
