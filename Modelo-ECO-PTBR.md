# 📘 ECO Técnica — Modelo Padronizado

> Documento técnico padrão para controle e rastreabilidade de alterações em modelos industriais.

---

## 1. 📦 Modelos Aplicados  
[Inserir lista completa com variações de nomenclatura, SKD/CKD, regionais]

## 2. 📅 Data de Aplicação  
Exemplo: Imediata / Após aprovação / Evento PA/PV / Data específica

## 3. 🔄 Tipo de Mudança  
- Mudança Casada: `Sim` / `Não`  
- Rework Necessário: `Sim` / `Não`

## 4. 🎯 Motivo da Mudança  
Descrição objetiva e técnica — ex.: ajuste de BOM, atualização de SW, correção de processo etc.

## 5. 🧠 Detalhamento Técnico  
**5.1 Componentes Impactados**  
Exemplo: SAA30114913 → SAA30114915  

**5.2 Versões de Software / QPA / Consumo**  
App History: 1073  
Checksum: 0552A796  

**5.3 ECO HQ / Códigos de Referência**  
EKMP700810, DKLP300437, EKLO200699, etc.

## 6. 🏭 Local de Aplicação  
Área específica onde a mudança será implementada: PCB Main, LCM, SMT, Pulp Pack etc.

## 7. 📝 Comentários e Observações  
- Diferenças entre versões anteriores  
- Status dos modelos (EOL, sem plano de produção)  
- Impactos esperados na produção e testes

## 8. 🧩 Ações por Área  
- RnD: Realizar validações / Atualizar instruções de trabalho  
- PE/MFG: Ajustar processo / Usar novo método ou versão / Acionar instrumentação  
- IQC/OQC/DQA/SQA: Realizar inspeções / Testes PMP / Homologações  
- PCM/SMT: Controlar estoque / Manutenção de WO / Aplicar submateriais conforme ECO  
- Instrumentação / Monitoramento / ST/LB: Suporte técnico / Check Option / Planejamento de tempo  
- Materiais: Para ciência / controle de consumo

## 9. 📎 Anexos  
- Instruções de trabalho  
- Comparativo BOM (As-Is x To-Be)  
- Relatórios de teste / ECO HQ  
- Fumisso / Documentos de validação



---

# 🗃️ ECO Técnica — Banco de Dados & Estrutura em Markdown
> Este documento descreve como os dados padronizados do modelo ECO podem ser representados em tabelas Markdown e posteriormente estruturados em um banco de dados relacional.

---

## 1. 📦 Tabela: eco_documents

| Campo               | Tipo      | Descrição                                      |
|---------------------|-----------|------------------------------------------------|
| id                  | INT (PK)  | Identificador único do ECO                     |
| document_title      | VARCHAR   | Título do documento técnico                    |
| applied_models      | TEXT      | Lista de modelos SKD/CKD aplicáveis            |
| implementation_date | DATE      | Data de aplicação da mudança                   |
| is_coupled_change   | BOOLEAN   | Mudança casada (`true` = sim / `false` = não)  |
| requires_rework     | BOOLEAN   | Rework necessário (`true` / `false`)           |
| change_reason       | TEXT      | Descrição técnica do motivo da mudança         |
| application_area    | VARCHAR   | Local de aplicação (PCB, LCM, etc.)            |
| comments            | TEXT      | Observações gerais do ECO                      |

---

## 2. 🔧 Tabela: technical_details

| Campo            | Tipo      | Descrição                                      |
|------------------|-----------|------------------------------------------------|
| id               | INT (PK)  | Identificador técnico                          |
| eco_id           | INT (FK)  | Referência ao ECO principal                    |
| component_from   | VARCHAR   | Código antigo do componente                    |
| component_to     | VARCHAR   | Código novo do componente                      |
| app_history      | VARCHAR   | Histórico de versão                            |
| checksum         | VARCHAR   | Código checksum para validação                 |
| reference_codes  | TEXT      | Códigos ECO HQ ou relacionados                 |

---

## 3. 🧩 Tabela: department_actions

| Campo            | Tipo      | Descrição                                       |
|------------------|-----------|-------------------------------------------------|
| id               | INT (PK)  | Identificador                                   |
| eco_id           | INT (FK)  | Referência ao documento ECO                    |
| department_name  | VARCHAR   | Nome da área responsável (RnD, MFG, IQC...)     |
| action_detail    | TEXT      | Descrição das ações planejadas/realizadas       |

---

## 4. 📎 Tabela: attachments

| Campo            | Tipo      | Descrição                                       |
|------------------|-----------|-------------------------------------------------|
| id               | INT (PK)  | Identificador                                   |
| eco_id           | INT (FK)  | Referência ao documento ECO                    |
| attachment_type  | VARCHAR   | Tipo de anexo (BOM, relatório, instrução, etc.) |
| file_path        | VARCHAR   | Caminho ou URL para o arquivo anexado           |

---

# 📘 Modelo Entidade-Relacionamento (ER)

Este modelo representa as relações entre as tabelas de uma estrutura de engenharia que utiliza documentos de alteração (ECO).

---

## 🧱 Tabela Principal: `eco_documents`

Contém os dados principais da solicitação de alteração de engenharia.

---

## 🔗 Relacionamentos e Cardinalidades

### 🔹 `eco_documents` → `technical_details`
- **Tipo**: 1:N (Um para Muitos)
- **Descrição**: Um ECO pode possuir vários detalhes técnicos.
- **Chave Estrangeira**: `technical_details.eco_id` → `eco_documents.id`

### 🔹 `eco_documents` → `department_actions`
- **Tipo**: 1:N (Um para Muitos)
- **Descrição**: Um ECO pode envolver múltiplos departamentos com diferentes ações.
- **Chave Estrangeira**: `department_actions.eco_id` → `eco_documents.id`

### 🔹 `eco_documents` → `attachments`
- **Tipo**: 1:N (Um para Muitos)
- **Descrição**: Um ECO pode conter vários arquivos anexos.
- **Chave Estrangeira**: `attachments.eco_id` → `eco_documents.id`

---

## 🧠 Estrutura Visual Simplificada

```text
eco_documents (1)
   ├── technical_details (N)
   ├── department_actions (N)
   └── attachments (N)
```
---


## 📌 Observações sobre uso em BD:

- Todas as tabelas possuem relacionamento via chave estrangeira (`eco_id`) para manter integridade e rastreabilidade.
- Os campos `TEXT` podem ser usados para informações descritivas que variam bastante em tamanho.
- Os campos `BOOLEAN` permitem lógica condicional no front-end (ex.: mostrar “⚠️ Rework”).
- Essa modelagem é compatível com bancos como MySQL, PostgreSQL, SQLite e pode ser facilmente traduzida para JSON se o sistema for NoSQL.
