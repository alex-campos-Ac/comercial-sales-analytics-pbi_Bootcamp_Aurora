# 📊 BI Analytics - Rede Aurora Odontologia

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Data Modeling](https://img.shields.io/badge/Modelagem_de_Dados-4CAF50?style=for-the-badge)

## 📌 Visão Geral do Projeto
Este projeto consiste no desenvolvimento de uma solução completa de Business Intelligence (BI) no Power BI para a **Rede Aurora Odontologia**, desenvolvido como case prático durante o **Bootcamp Educadados**. 

O objetivo principal é transformar dados brutos em insights acionáveis, abrangendo análises financeiras, operacionais, comerciais e de relacionamento da rede de clínicas, permitindo à diretoria uma tomada de decisão ágil e baseada em dados.

🔗 **[Acessar o Dashboard Interativo (Fase 1)](https://app.powerbi.com/view?r=eyJrIjoiMmM4Njg0YTktNjNjYS00ZDcyLTgyM2MtM2RiYjgwZmQyN2ZhIiwidCI6IjE1ZWVlYjY4LWNjMzAtNDEwNS1iYzIxLTYzMGJjMTMyNmQ2ZCJ9)**
🔗 **[Acessar a Documentação no Google Drive](https://drive.google.com/drive/folders/1PtpgE8dY0YrzVm7pclqVQW31FUXlv9Yh?usp=drive_link)**

---

## 🚀 Fases de Desenvolvimento

O projeto está estruturado em 5 fases evolutivas (Novembro/2026 a Janeiro/2027).

- [x] **Fase 1: Fundação e Análise de Vendas (Concluída em 09/11/2026)**
  - Modelagem dimensional inicial (Star Schema).
  - Criação de métricas de faturamento (Vendas e Recebimentos).
  - Análise de atingimento de metas comerciais (por filial, vendedor, produto/serviço).
- [ ] **Fase 2: Funil de Orçamentos e Marketing (Em andamento - Prazo: 23/11/2026)**
  - Expansão do modelo de dados para orçamentos e mídias.
  - Cálculo de Taxa de Conversão e Ticket Médio por canal de atração.
  - Visão demográfica dos pacientes.
- [ ] **Fase 3: *A definir (Requisitos em breve)***
- [ ] **Fase 4: *A definir (Requisitos em breve)***
- [ ] **Fase 5: *A definir (Requisitos em breve)***

---

## 🗄️ Modelagem de Dados

O projeto utiliza um modelo híbrido combinando **Star Schema** (Esquema em Estrela) e **Snowflake** (Floco de Neve) para otimizar a performance no Power BI. A direção dos filtros flui em cardinalidade `1:*` das tabelas Dimensão para as tabelas Fato.

### 🔹 Tabelas Dimensão (Contexto)
* `calendario`: Tabela de datas contínua.
* `filiais` / `cidades`: Hierarquia de localidade das unidades.
* `profissionais` / `vendedores` / `usuarios`: Equipe da clínica.
* `grupos_servico` / `servicos`: Catálogo de produtos.
* `clientes`: Dados demográficos dos pacientes (Fase 2).
* `midias`: Canais de atração e marketing (Fase 2).

### 🔸 Tabelas Fato (Eventos)
* `vendas` / `itens_venda`: Registros de faturamento e serviços prestados.
* `metas_valor` / `metas_quantidade`: Metas estipuladas por níveis independentes.
* `orcamentos` / `itens_orcamento`: Controle de avaliações e emissão de orçamentos (Fase 2).

> **Nota de Arquitetura:** O relacionamento entre a Fato `orcamentos` e a Fato `vendas` ocorre de forma opcional (1:1), existindo apenas quando o orçamento é aprovado, garantindo a rastreabilidade da conversão.

---

## 📈 Principais Métricas (DAX)

Algumas das principais medidas desenvolvidas para responder às perguntas de negócio:

**Comercial e Faturamento (Fase 1):**
* `Total Vendas`: Faturamento bruto abatido de descontos.
* `Atingimento de Meta (%)`: Comparativo entre o realizado e o planejado nos níveis de Produto, Serviço, Vendedor e Profissional.

**Funil e Conversão (Fase 2 - Em desenvolvimento):**
* `Taxa de Conversão (%)`: (Orçamentos Aprovados / Total de Orçamentos).
* `Ticket Médio por Canal`: (Faturamento Total / Qtd. de Vendas) filtrado pelas dimensões de Mídia.

---

## 🛠️ Ferramentas Utilizadas
* **Microsoft Power BI:** ETL (Power Query), Modelagem de Dados, DAX e Data Visualization.
* **Microsoft Excel:** Fontes de dados estruturadas.

---
*Projeto desenvolvido por [Seu Nome] durante o Bootcamp Educadados.*