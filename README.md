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
- [Funcionalidades e Recursos do Dashboard](#-funcionalidades-e-recursos-do-dashboard)
- [Contato](#-contato)

---

# 🎯 Visão Geral do Projeto

O objetivo deste projeto foi desenvolver uma aplicação web analítica autossuficiente — composta por arquivos leves e sem dependência de servidores complexos — capaz de ler, tratar e exibir dados dinâmicos de vendas diretamente no navegador.

A interface foi projetada sob conceitos avançados de UI/UX (estética *Bento Box*, *Glassmorphism* e suporte nativo a temas *Dark/Light*), oferecendo aos usuários e recrutadores uma ferramenta de visualização executiva fluida, responsiva e rica em recursos analíticos.

---

# 🏗️ Arquitetura e Componentes da Solução

O fluxo de dados e renderização acontece inteiramente no lado do cliente (*Client-Side Rendering*):

```text
+-----------------+        +-----------------------+        +------------------------+
|  Planilha Bruta | ---->  |  Parser SheetJS (XLSX)| ---->  | Motor de Filtros & DB  |
|  (vendas.xlsx)  |        |  (Leitura Binária)    |        | (JavaScript Nativo)    |
+-----------------+        +-----------------------+        +------------------------+
                                                                         |
                                                                         v
                                                            +------------------------+
                                                            | Renderização Dinâmica  |
                                                            | (Chart.js + DOM HTML)  |
                                                            +------------------------+

Ingestão & Parsing (SheetJS): Leitura assíncrona do arquivo Excel (vendas.xlsx) diretamente no navegador, convertendo linhas brutas em objetos estruturados via ArrayBuffer.

Motor Analítico & Estado: Processamento em tempo real de agregações, filtros globais por múltiplos parâmetros, faixas de datas, busca textual e cálculos de variações percentuais.

Camada Visual (Chart.js & CSS Variables): Geração dinâmica de gráficos interativos (linhas temporais, roscas de market share, barras horizontais de ranking) com adaptação instantânea de paletas para modo claro ou escuro.

---

# 🛠️ Destaques Técnicos & UI/UX

Design System Moderno: Estrutura visual baseada em grids do tipo Bento Box, proporcionando uma hierarquia clara de informações e cartões de KPI com mini-gráficos de tendência (sparklines).

- Mecanismo de Filtros Cruzados: Filtragem instantânea por marcas, canais de venda, formas de pagamento, estados (UF), vendedores e intervalos de datas personalizados ou predefinidos (YTD, 7d, 30d, 90d).
- Modo Escuro / Claro Dinâmico: Alternância de temas em tempo real com persistência de preferência via localStorage.
- Exportação e Relatórios: Funcionalidade nativa para exportar os dados filtrados em formato .CSV estruturado ou gerar uma visualização otimizada para impressão física/PDF (window.print).

Resiliência e Fallback de Carga: Sistema de carregamento inteligente que detecta automaticamente restrições de CORS em servidores locais, disponibilizando um seletor manual de arquivos (vendas_2.xlsx) para garantir que o projeto funcione em qualquer ambiente.

---

# 📂 Estrutura do Repositório
.
├── index.html         # Aplicação completa (HTML, CSS customizado e Lógica JS)
├── vendas_2.xlsx      # Base de dados de vendas utilizada para alimentação do BI
└── README.md          # Documentação oficial do repositório

---

# 🚀 Tecnologias Utilizadas

# Linguagens: HTML5 Semântico, CSS3 (Variáveis, Flexbox, Grid) e JavaScript (ES6+).

# Bibliotecas de Terceiros:
- Chart.js (v3.9.1) — Renderização de gráficos dinâmicos.
- SheetJS (xlsx) (v0.18.5) — Leitura e interpretação de arquivos Excel.

# Tipografia: Google Fonts (Plus Jakarta Sans e JetBrains Mono).

# Ambiente: Execução 100% Client-Side (compatível com qualquer navegador moderno).

---

# 📥 Como Baixar e Executar o Projeto
Para testar e visualizar o projeto em funcionamento na sua máquina local, siga os passos abaixo:

1. Clonar ou Baixar o Repositório
Baixe os arquivos do projeto (index.html e vendas_2.xlsx) mantendo-os juntos na mesma pasta no seu computador.

2. Abrir o Projeto
Como o dashboard processa dados locais via JavaScript, você pode executá-lo de duas formas:

Forma Direta: Dê um duplo clique no arquivo index.html para abri-lo diretamente no seu navegador padrão.

Ambiente de Servidor Local (Recomendado): Se preferir evitar alertas de segurança de CORS de alguns navegadores ao carregar arquivos locais, abra a pasta do projeto no VS Code e utilize a extensão Live Server, ou execute um servidor simples via terminal:

# Python 3
python -m http.server 8000
(Em seguida, acesse http://localhost:8000 no seu navegador).

3. Validação Automática
O dashboard localizará o arquivo vendas_2.xlsx automaticamente no diretório, processará os registros, calculará os KPIs e renderizará todos os gráficos de performance de vendas instantaneamente. Caso utilize o arquivo em modo estrito sem servidor, utilize o botão seletor integrado que aparecerá na tela para carregar o arquivo .xlsx.

---

# 👤 Contato

💼 LinkedIn: linkedin.com/in/emersonfariasbr
🌐 Site/Portfólio: emersonfarias.com.br
💻 GitHub: @emersonfariasmcz
📸 Instagram: @emersonfarias.dev
🎥 YouTube: @emersonfariasdev

---

Se este projeto ajudou você ou serviu de inspiração, não se esqueça de deixar uma ⭐️!
