# analise-estoque-powerbi
analise-estoque-powerbi
# Dashboard de Análise de Estoque Parado
<p align="center">
  <img src="https://img.shields.io/badge/Status-Concluído-brightgreen?style=for-the-badge" alt="Status do Projeto: Concluído"/>
  <img src="https://img.shields.io/badge/Power%20BI-Desktop-555?style=for-the-badge&logo=powerbi&logoColor=yellow" alt="Ferramenta: Power BI"/>
  <img src="https://img.shields.io/badge/Linguagem-DAX-0078D4?style=for-the-badge" alt="Linguagem: DAX"/>
  <img src="https://img.shields.io/badge/ETL-Power%20Query-01B8AA?style=for-the-badge" alt="ETL: Power Query"/>
</p>

![Capa do Dashboard](URL_DA_SUA_MELHOR_IMAGEM_DA_PÁGINA_1)

## 🎯 Descrição do Projeto

Este projeto foi desenvolvido para analisar o problema de estoque sem giro em uma empresa de distribuição. O objetivo é transformar dados brutos de inventário em um dashboard interativo que permita à gestão identificar rapidamente os principais focos de capital empatado, analisar as causas raiz por categoria e marca, e tomar decisões estratégicas para otimizar o inventário.

---

## 🚀 Funcionalidades e Análises Principais

* **KPIs Estratégicos:** Análise do valor total parado, quantidade de SKUs afetados e um detalhamento do Ticket Médio por Curva de Relevância (A, B, C).
* **Análise de Pareto (Curva ABC):** Segmentação automática dos produtos nas curvas A, B e C para focar os esforços nos itens que representam 80% do valor parado.
* **Navegação por Drill-through:** Funcionalidade que permite uma jornada de análise do resumo geral (por categoria) para uma visão detalhada (por produto) com um simples clique.
* **Tooltips Interativos:** Dicas de ferramenta personalizadas que mostram a lista de SKUs específicos de uma marca ao passar o mouse, aprofundando a análise sem poluir a tela.
* **"Tabela Inteligente" com Formatação Condicional:** Uma tabela de dados que usa cores, ícones e barras para sinalizar visualmente a prioridade, o risco de volume e a rentabilidade de cada item.

---

## 🛠️ Ferramentas e Conceitos Utilizados

* **Power BI Desktop:** Ferramenta principal para desenvolvimento, modelagem e criação dos visuais.
* **DAX (Data Analysis Expressions):** Utilizado para criar todas as métricas, classificações (Curva ABC) e as lógicas de interatividade avançada.
* **Power Query:** Utilizado para a conexão, limpeza e tratamento inicial dos dados a partir dos arquivos CSV.
* **Design de UI/UX:** Aplicação de conceitos de hierarquia visual, paleta de cores consistente e formatação condicional para criar uma experiência de usuário intuitiva.

---

## 📊 Estrutura do Dashboard

O relatório é composto por duas páginas principais e páginas de suporte para tooltips:

### Página 1: Resumo Executivo
Visão macro do problema, ideal para a diretoria. Responde "Qual o tamanho do problema e onde ele está concentrado?".
#### Página 1: Visão Geral

![Visão Geral](assets/dashboard_resumo_executivo.png)

### Página 2: Análise Detalhada
Página de ação para gestores. Acessada via drill-through, permite a investigação em nível de produto e categoria. Responde "Quais são os itens e marcas exatos que precisam de atenção?".

![Análise Detalhada](assets/dashboard_analise_detalhada.png)

---

## 💡 Medida DAX de Destaque

Uma das medidas mais interessantes do projeto é a que calcula o Ticket Médio para uma curva específica, como a Curva A.

```dax
Ticket Médio Curva A =
CALCULATE (
    [Ticket Médio Parado],
    'Dim_produto'[Classificação ABC] = "A"
)
```

## Autor
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Carlos%20Vinícius-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/carlos-vinicius-nascimento-de-jesus/)
[![GitHub](https://img.shields.io/badge/GitHub-Carllux-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Carllux/)
