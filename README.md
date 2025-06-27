# 📊 Propostas de Projeto – DX Academy

Este repositório contém propostas de sistemas web completos desenvolvidos com **AngularJS 1.8** no front-end e **FastAPI** no back-end, com banco de dados relacional (**PostgreSQL**). Todos os projetos seguem os seguintes requisitos:

## ✅ Requisitos Atendidos

- Login com autenticação JWT
- Controle de permissões (RBAC)
- Mínimo de 7 telas
- Pelo menos 1 CRUD completo
- Dashboard funcional com gráficos (entregue até final de julho)
- Relatórios semanais de progresso
- Back-end e front-end completos

---

## 🔹 Proposta 1 – FlowDocs Teams

> Sistema colaborativo de documentação e execução de testes

| Item | Descrição |
|------|----------|
| **Objetivo** | Centralizar documentos técnicos e testes com rastreabilidade |
| **Público-alvo** | Equipes ágeis e times de engenharia |
| **Telas** | Login, Dashboard, Projetos, Documentos (CRUD), Casos de Teste (CRUD), Execuções, Relatórios, Administração |
| **Permissões** | Admin, Editor, Leitor |
| **Stack** | Angular 17 + Material • NestJS • MySQL |
| **CRUD mínimo** | Documentos, Casos de Teste |
| **Relatórios semanais** | Aprovação de testes, bugs abertos/fechados |
| **Dashboard** | Cobertura de testes, tempo médio entre versões |

**🔍 Concorrente Popular:**  
O **Confluence (Atlassian)** é amplamente usado para colaboração técnica e documentação. O FlowDocs Teams traz uma abordagem leve, com testes integrados e rastreabilidade, ideal para squads que desejam autonomia e controle completo sobre os dados.

---

## 🔹 Proposta 2 – StorePro 360

> Gestão de estoque, pedidos e logística para PMEs

| Item | Descrição |
|------|----------|
| **Objetivo** | Reunir estoque, vendas e reabastecimento num único sistema |
| **Público-alvo** | Pequenos e médios comércios |
| **Telas** | Login, Dashboard, Produtos (CRUD), Pedidos (CRUD), Clientes, Reabastecimento, Relatórios, Configurações |
| **Permissões** | Admin, Operador, Visualizador |
| **Stack** | React 19 + Spring Boot • PostgreSQL |
| **CRUD mínimo** | Produtos, Pedidos |
| **Relatórios semanais** | Vendas diárias, rupturas |
| **Dashboard** | KPIs: ticket médio, giro de estoque |

**🔍 Concorrente Popular:**  
O **Bling ERP** oferece um sistema completo para gestão de pequenos negócios com emissão de nota fiscal. O StorePro 360 é uma alternativa open source ideal para aprendizagem técnica e adaptação conforme a realidade do cliente.

---

## 🔹 Proposta 3 – EventHub

> Plataforma de agendamento e avaliação de eventos corporativos

| Item | Descrição |
|------|----------|
| **Objetivo** | Gerenciar eventos internos com check-in e avaliação |
| **Público-alvo** | RHs e líderes de treinamento |
| **Telas** | Login, Dashboard, Eventos (CRUD), Inscrições, Check-in QR, Avaliações (CRUD), Relatórios, Administração |
| **Permissões** | Super Admin, Organizador, Participante |
| **Stack** | Vue 4 + Laravel • MariaDB |
| **CRUD mínimo** | Eventos, Avaliações |
| **Relatórios semanais** | NPS, taxa de presença |
| **Dashboard** | Heat-map, comparativos de satisfação |

**🔍 Concorrente Popular:**  
O **Sympla** domina o mercado de eventos abertos. O EventHub foca em eventos **internos corporativos**, com funcionalidades que atendem diretamente à área de RH e sem cobrança por inscrição.

---

## 🔹 Proposta 4 – LegalDoc

> Sistema jurídico de controle de processos e contratos

| Item | Descrição |
|------|----------|
| **Objetivo** | Acompanhar prazos, processos e documentos jurídicos |
| **Público-alvo** | Escritórios de advocacia |
| **Telas** | Login, Dashboard, Processos (CRUD), Contratos (CRUD), Clientes, Agenda, Relatórios, Usuários |
| **Permissões** | Admin, Advogado, Estagiário |
| **Stack** | Vue 4 + Laravel 11 • MySQL |
| **CRUD mínimo** | Processos, Contratos |
| **Relatórios semanais** | Casos vencidos, clientes ativos |
| **Dashboard** | Alertas de vencimento, produtividade |

**🔍 Concorrente Popular:**  
O **SAJ ADV** é um sistema jurídico robusto usado por grandes escritórios. O LegalDoc propõe um sistema mais leve, direto ao ponto, ideal para quem deseja controle simples, prático e sem mensalidades.

---

## 🔹 Proposta 5 – StockFlow

> Controle de estoque com alertas e relatórios

| Item | Descrição |
|------|----------|
| **Objetivo** | Automatizar o monitoramento e reposição de estoque |
| **Telas** | Login, Dashboard, Produtos (CRUD), Entradas, Saídas, Fornecedores, Categorias, Relatórios |
| **Permissões** | Admin, Estoquista, Consulta |
| **Stack** | AngularJS + FastAPI + PostgreSQL |
| **Relatórios semanais** | Itens críticos, valor em estoque |
| **Dashboard** | Gráficos de giro de estoque e categorias |

**🔍 Concorrente Popular:**  
O **Tiny ERP** oferece funcionalidades semelhantes, porém com custo mensal. O StockFlow oferece controle total do código, sendo ideal para desenvolvedores ou negócios que precisam de uma solução flexível e gratuita.

---

## 🔹 Proposta 6 – FinTrack

> Plataforma de controle financeiro para PMEs e autônomos

| Item | Descrição |
|------|----------|
| **Objetivo** | Organizar finanças com metas e visualização clara de fluxo |
| **Telas** | Login, Dashboard, Receitas (CRUD), Despesas (CRUD), Categorias, Contas, Metas, Relatórios, Administração |
| **Permissões** | Admin, Financeiro, Analista |
| **Stack** | AngularJS + FastAPI + PostgreSQL + Chart.js |
| **Relatórios semanais** | Fluxo de caixa, metas, categorias |
| **Dashboard** | Saldo projetado, comparativo de metas |

**🔍 Concorrente Popular:**  
O **Conta Azul** é amplamente usado por pequenos empreendedores no Brasil. O FinTrack é uma alternativa didática e gratuita, permitindo customizações e foco em aprendizado técnico.

---

## 🔹 Proposta 7 – MiniERP Estoque & Finanças

> Mini ERP com módulos de vendas, estoque e financeiro

| Item | Descrição |
|------|----------|
| **Objetivo** | Oferecer uma solução unificada para PMEs |
| **Telas** | Login, Dashboard, Produtos (CRUD), Vendas (CRUD), Clientes, Fornecedores, Contas a Pagar/Receber, Relatórios, Configurações, Usuários |
| **Permissões** | Admin, Estoquista, Comercial, Financeiro |
| **Stack** | AngularJS + FastAPI + PostgreSQL + Tailwind |
| **Relatórios semanais** | Vendas, lucro, inadimplência |
| **Dashboard** | KPIs em tempo real e integração de módulos |

**🔍 Concorrente Popular:**  
O **Omie** é um ERP bastante completo no mercado brasileiro. O MiniERP proposto tem foco educacional e total flexibilidade de código para que o aluno compreenda na prática como funciona a integração de setores no backend e frontend.

---

## 📅 Cronograma-base para todas as propostas

| Semana | Entregas |
|--------|----------|
| **S1 (27/06 – 03/07)** | Definição de escopo, wireframes, setup do repositório |
| **S2 (04/07 – 10/07)** | Login com JWT, controle de permissões (RBAC) |
| **S3 (11/07 – 17/07)** | CRUD principal (Produtos / Receitas / Processos etc) |
| **S4 (18/07 – 24/07)** | CRUD secundário, relacionamentos, validações |
| **S5 (25/07 – 31/07)** | Dashboard com gráficos + relatórios PDF/CSV |
| **Buffer** | Testes finais, documentação e deploy |

📌 **Relatórios semanais**: entregues toda **segunda-feira**, contendo:
- Markdown do progresso
- Print das telas implementadas
- Checklist das metas semanais
