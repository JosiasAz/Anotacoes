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

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Centralizar documentos técnicos e testes com rastreabilidade             |
| **Público-alvo** | Equipes ágeis e times de engenharia                                       |
| **Telas**        | Login, Dashboard, Projetos, Documentos (CRUD), Casos de Teste (CRUD), Execuções, Relatórios, Administração |
| **Permissões**   | Admin, Editor, Leitor                                                     |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL                                      |
| **CRUD mínimo**  | Documentos, Casos de Teste                                                |
| **Relatórios**   | Aprovação de testes, bugs abertos/fechados                               |
| **Dashboard**    | Cobertura de testes, tempo médio entre versões                            |

🔍 **Concorrente Popular:**  
O Confluence (Atlassian) é amplamente utilizado para documentação e colaboração. O FlowDocs Teams oferece uma alternativa técnica voltada para squads com foco em rastreabilidade e integração de testes.

---

## 🔹 Proposta 2 – StorePro 360

> Gestão de estoque, pedidos e logística para PMEs

| Item             | Descrição                                                                  |
|------------------|---------------------------------------------------------------------------|
| **Objetivo**     | Unificar controle de estoque, vendas e reabastecimento                     |
| **Público-alvo** | Pequenos e médios comércios                                                |
| **Telas**        | Login, Dashboard, Produtos (CRUD), Pedidos (CRUD), Clientes, Reabastecimento, Relatórios, Configurações |
| **Permissões**   | Admin, Operador, Visualizador                                               |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL                                       |
| **CRUD mínimo**  | Produtos, Pedidos                                                          |
| **Relatórios**   | Vendas diárias, rupturas                                                   |
| **Dashboard**    | Ticket médio, giro de estoque                                              |

🔍 **Concorrente Popular:**  
O Bling ERP oferece uma solução robusta para PMEs. O StorePro 360 propõe uma solução educacional gratuita, ideal para personalizações e aprendizado técnico.

---

## 🔹 Proposta 3 – EventHub

> Plataforma de agendamento e avaliação de eventos internos

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Gerenciar eventos corporativos com check-in e avaliação                   |
| **Público-alvo** | Setores de RH e líderes de treinamento                                     |
| **Telas**        | Login, Dashboard, Eventos (CRUD), Inscrições, Check-in QR, Avaliações (CRUD), Relatórios, Administração |
| **Permissões**   | Super Admin, Organizador, Participante                                     |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL                                       |
| **CRUD mínimo**  | Eventos, Avaliações                                                       |
| **Relatórios**   | NPS, taxa de presença                                                     |
| **Dashboard**    | Heat-map, comparativos de satisfação                                       |

🔍 **Concorrente Popular:**  
O Sympla domina eventos públicos, enquanto o EventHub atende necessidades corporativas com foco em privacidade e engajamento interno.

---

## 🔹 Proposta 4 – LegalDoc

> Sistema de gestão de processos e contratos jurídicos

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Acompanhar prazos, documentos e processos jurídicos                        |
| **Público-alvo** | Escritórios de advocacia e departamentos jurídicos                         |
| **Telas**        | Login, Dashboard, Processos (CRUD), Contratos (CRUD), Clientes, Agenda, Relatórios, Usuários |
| **Permissões**   | Admin, Advogado, Estagiário                                                |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL                                       |
| **CRUD mínimo**  | Processos, Contratos                                                      |
| **Relatórios**   | Casos vencidos, clientes ativos                                           |
| **Dashboard**    | Alertas de vencimento, produtividade                                      |

🔍 **Concorrente Popular:**  
O SAJ ADV é referência no mercado jurídico. O LegalDoc oferece uma abordagem prática, sem dependência de terceiros e ideal para ambientes menores.

---

## 🔹 Proposta 5 – StockFlow

> Controle de estoque com alertas e relatórios em tempo real

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Automatizar o controle e a reposição de estoque                           |
| **Público-alvo** | Micro e pequenos negócios                                                 |
| **Telas**        | Login, Dashboard, Produtos (CRUD), Entradas, Saídas, Fornecedores, Categorias, Relatórios |
| **Permissões**   | Admin, Estoquista, Consulta                                               |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL                                       |
| **Relatórios**   | Itens críticos, valor de estoque                                          |
| **Dashboard**    | Gráficos de giro, volume e categorias                                     |

🔍 **Concorrente Popular:**  
O Tiny ERP oferece funcionalidades similares com mensalidade. O StockFlow permite total controle e modificação do código, sendo ideal para aprendizado e adaptação.

---

## 🔹 Proposta 6 – FinTrack

> Plataforma de controle financeiro com metas e previsões

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Organizar finanças e visualizar o fluxo com clareza                       |
| **Público-alvo** | Autônomos, MEIs e PMEs                                                    |
| **Telas**        | Login, Dashboard, Receitas (CRUD), Despesas (CRUD), Contas, Categorias, Metas, Relatórios, Administração |
| **Permissões**   | Admin, Financeiro, Analista                                               |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL • Chart.js                           |
| **Relatórios**   | Fluxo de caixa, metas, categorias                                         |
| **Dashboard**    | Saldo projetado, comparativo mensal                                       |

🔍 **Concorrente Popular:**  
O Conta Azul é bastante conhecido no Brasil. O FinTrack oferece um caminho mais didático e customizável para ensino de controle financeiro digital.

---

## 🔹 Proposta 7 – MiniERP Estoque & Finanças

> Mini ERP com foco em vendas, estoque e financeiro

| Item             | Descrição                                                                 |
|------------------|--------------------------------------------------------------------------|
| **Objetivo**     | Unificar módulos essenciais de gestão para PMEs                           |
| **Público-alvo** | Pequenos negócios e profissionais em transição digital                    |
| **Telas**        | Login, Dashboard, Produtos (CRUD), Vendas (CRUD), Contas a Pagar/Receber, Clientes, Fornecedores, Usuários, Relatórios, Configurações |
| **Permissões**   | Admin, Estoquista, Comercial, Financeiro                                  |
| **Stack**        | AngularJS 1.8 • FastAPI • PostgreSQL • Tailwind CSS                       |
| **Relatórios**   | Lucro mensal, inadimplência, vendas por cliente                           |
| **Dashboard**    | KPIs em tempo real e integração entre áreas                               |

🔍 **Concorrente Popular:**  
O Omie é uma das soluções mais completas para PMEs. O MiniERP é uma base ideal para estudos técnicos sobre integração de múltiplos módulos em aplicações web full-stack.

---

## 📅 Cronograma-base para todas as propostas

| Semana             | Entregas                                                                   |
|--------------------|----------------------------------------------------------------------------|
| S1 (27/06 – 03/07) | Definição de escopo, wireframes, setup do repositório                      |
| S2 (04/07 – 10/07) | Login com JWT, controle de permissões (RBAC)                               |
| S3 (11/07 – 17/07) | CRUD principal (Produtos / Receitas / Processos etc)                       |
| S4 (18/07 – 24/07) | CRUD secundário, relacionamentos, validações                               |
| S5 (25/07 – 31/07) | Dashboard com gráficos + relatórios PDF/CSV                                |
| Buffer             | Testes finais, documentação e deploy                                       |

---

## 📌 Relatórios semanais

Entregues toda segunda-feira contendo:

- ✔ Markdown do progresso  
- ✔ Print das telas implementadas  
- ✔ Checklist das metas semanais  
