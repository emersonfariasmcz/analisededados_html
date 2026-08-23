# 📊 Dashboard Analítico de Vendas · Web BI

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-Interactive%20Charts-FF6384?style=for-the-badge&logo=chart.js&logoColor=white)](https://www.chartjs.org/)
[![SheetJS](https://img.shields.io/badge/SheetJS-XLSX%20Parser-173F5F?style=for-the-badge&logo=sheet.js&logoColor=white)](https://sheetjs.com/)
[![HTML5](https://img.shields.io/badge/HTML5-Semantic-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)

Projeto de **Business Intelligence (BI) e Data Visualization Frontend**, consistindo em um painel interativo de alta performance voltado para a análise executiva de KPIs comerciais, faturamento, ticket médio e distribuição geográfica de vendas a partir de planilhas Excel.

---

## 📌 Sumário
- [Visão Geral do Projeto](#-visão-geral-do-projeto)
- [Arquitetura e Componentes da Solução](#-arquitetura-e-componentes-da-solução)
- [Destaques Técnicos & UI/UX](#-destaques-técnicos--uiux)
- [Estrutura do Repositório](#-estrutura-do-repositório)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Como Baixar e Executar o Projeto](#-como-baixar-e-executar-o-projeto)
- [Contato](#-contato)

---

## 🎯 Visão Geral do Projeto

O objetivo deste projeto foi desenvolver uma aplicação web analítica autossuficiente — composta por arquivos leves e sem dependência de servidores complexos — capaz de ler, tratar e exibir dados dinâmicos de vendas diretamente no navegador.

A interface foi projetada sob conceitos avançados de UI/UX (estética *Bento Box*, *Glassmorphism* e suporte nativo a temas *Dark/Light*), oferecendo aos usuários e recrutadores uma ferramenta de visualização executiva fluida, responsiva e rica em recursos analíticos.

---

## 🏗️ Arquitetura e Componentes da Solução

O fluxo de dados e renderização acontece inteiramente no lado do cliente (*Client-Side Rendering*):

```text
+-----------------+        +-----------------------+        +------------------------+
|  Planilha Bruta | ---->  |  Parser SheetJS (XLSX)| ---->  | Motor de Filtros & DB  |
|  (vendas_2.xlsx)|        |  (Leitura Binária)    |        | (JavaScript Nativo)    |
+-----------------+        +-----------------------+        +------------------------+
                                                                         |
                                                                         v
                                                            +------------------------+
                                                            | Renderização Dinâmica  |
                                                            | (Chart.js + DOM HTML)  |
                                                            +------------------------+
