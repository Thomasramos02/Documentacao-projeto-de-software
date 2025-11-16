# 📘 Projeto de Software – Sistema de E-Commerce de Suplementos

Este repositório apresenta a modelagem completa de um sistema de e-commerce de suplementos, desenvolvido para a disciplina **Projeto de Software**.  
Inclui todos os artefatos exigidos no processo de análise e design, seguindo padrões **UML**.

---

## 📑 Sumário
- [Descrição Geral](#-descrição-geral)
- [Escopo do Sistema](#-escopo-do-sistema)
- [Casos de Uso](#-casos-de-uso)
- [Diagramas UML](#-diagramas-uml)
  - [Diagrama de Casos de Uso](#-diagrama-de-casos-de-uso)
  - [Diagrama de Classes](#-diagrama-de-classes)
  - [Diagramas de Sequência](#-diagramas-de-sequência)
  - [Diagramas de Comunicação](#-diagramas-de-comunicação)
  - [Diagramas de Estados](#-diagramas-de-estados)
  - [Diagrama de Componentes](#-diagrama-de-componentes)
  - [Diagrama de Implantação](#-diagrama-de-implantação)
- [Modelo de Dados](#-modelo-de-dados-der)
- [Mapeamento Objeto–Relacional](#-estratégias-de-mapeamento-objeto–relacional)
- [Tecnologias Sugeridas](#-tecnologias-sugeridas)
- [Autor](#-autor)

---

## 🧾 Descrição Geral

O sistema modelado representa um **e-commerce de suplementos**, permitindo que clientes:

- realizem compras online,
- acompanhem pedidos,
- gerenciem suas contas.

Administradores podem controlar produtos, usuários e pedidos.

A modelagem segue princípios de análise orientada a objetos, utilizando **UML** como linguagem padrão.

---

## 🎯 Escopo do Sistema

### 👤 Cliente
- Criar conta  
- Editar/Excluir conta  
- Realizar compras  
- Acompanhar status dos pedidos  

### 🛠️ Administrador
- Gerenciar produtos  
- Gerenciar pedidos  
- Gerenciar usuários  

---

## 📁 Casos de Uso

| ID | Caso de Uso | Atores | Descrição |
|----|--------------|--------|-----------|
| UC-01 | Finalizar Compra | Cliente | Concluir a compra de suplementos. |
| UC-02 | Acompanhar Pedido | Cliente | Consultar andamento da entrega. |
| UC-03 | Gerenciar Conta | Cliente/Admin | Criação, edição e exclusão de conta. |
| UC-03.1 | Criar Conta | Usuário | Criar uma nova conta. |
| UC-03.2 | Editar Conta | Usuário | Editar dados pessoais. |
| UC-03.3 | Excluir Conta | Usuário | Remover conta definitivamente. |
| UC-04 | Gerenciar Pedidos | Admin | Atualizar status, cancelar e visualizar pedidos. |
| UC-05 | Gerenciar Produtos | Admin | Incluir, remover e editar produtos. |

---

## 🧩 Diagramas UML

### 📌 Diagrama de Casos de Uso
Representa as interações entre usuários e funcionalidades do sistema.  
📁 `/diagrams/usecase/`

---

### 📌 Diagrama de Classes
Modelo estrutural representado com PlantUML.  
📁 `/diagrams/class/`

---

### 📌 Diagramas de Sequência
Diagramas disponíveis:

- Cliente finaliza compra  
- Cliente faz login  
- Admin gerencia produtos  
- Admin administra usuários  
- Cliente acompanha pedido  

📁 `/diagrams/sequence/`

---

### 📌 Diagramas de Comunicação
Fluxos representados:

- Cliente faz pedido  
- Cliente faz login  
- Admin gerencia usuários  

📁 `/diagrams/communication/`

---

### 📌 Diagramas de Estados
Estados representados:

- **Pedido:** Criado → Pago → Enviado → Entregue / Cancelado  
- **Conta do usuário**

📁 `/diagrams/state/`

---

### 📌 Diagrama de Componentes
Representa:

- Frontend  
- API Backend  
- Banco de Dados  

📁 `/diagrams/component/`

---

### 📌 Diagrama de Implantação
Mostra os ambientes onde o sistema é executado:

- Servidor Frontend  
- Servidor Backend  
- Banco de Dados  

📁 `/diagrams/deployment/`

---

## 📌 Modelo de Dados (DER)
Modelo contendo:

- Usuário  
- Produto  
- Pedido  
- Item_Pedido  
- Pagamento  

Com relacionamentos e cardinalidades.  
📁 `/diagrams/database/modelo_dados.puml`

---

## 🔄 Estratégias de Mapeamento Objeto–Relacional

| Classe      | Tabela        | Mapeamento |
|-------------|---------------|------------|
| Usuario     | usuario       | 1:1 direto |
| Produto     | produto       | 1:1 direto |
| Pedido      | pedido        | FK para usuário |
| ItemPedido  | item_pedido   | Tabela associativa Pedido × Produto |
| Pagamento   | pagamento     | 1:1 com Pedido |

**Padrões aplicados:**
- FK para associações **1:N**  
- Tabela intermediária para composição de itens  
- Enum para tipo de usuário  
- Normalização **3FN**

---

## 🛠️ Tecnologias Sugeridas

Embora o projeto seja de modelagem, uma implementação poderia usar:

### Backend
- Node.js  
- Spring Boot  
- Laravel  

### Frontend
- React  
- HTML/CSS/Bootstrap  

### Banco de Dados
- PostgreSQL  
- MySQL  

### UML
- PlantUML  
- Draw.io  

---

## 👨‍💻 Autor

**Thomas Ramos**  
PUC Minas — Engenharia de Software  
Disciplina: Projeto de Software  

---
