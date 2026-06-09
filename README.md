markdown

# 🛒 Dashboard de Vendas com Streamlit

<p align="left">
  <img src="https://shields.io" alt="Python">
  <img src="https://shields.io" alt="Streamlit">
  <img src="https://shields.io" alt="Pandas">
  <img src="https://shields.io" alt="Plotly">
</p>

Este é um projeto de um painel interativo de vendas desenvolvido em Python utilizando a biblioteca **Streamlit**. O objetivo é consolidar dados comerciais e apresentar métricas de receitas, quantidades de vendas e desempenho de vendedores por meio de gráficos dinâmicos.

## 🚀 Funcionalidades
- **Análise Dinâmica**: Abas separadas para avaliar Receitas, Quantidade de Vendas e Desempenho do Time.
- **Filtros Personalizados**: Segmentação de dados por região, ano e vendedores diretamente na barra lateral.
- **Gráficos Interativos**: Mapas de geolocalização e gráficos de barras/linhas construídos com **Plotly**.
- **Arquitetura Escalável**: Preparado para múltiplas páginas utilizando a estrutura integrada de navegação.

## 🛠️ Tecnologias Utilizadas
- **Python 3.12+**
- **Streamlit** (Interface e Layout)
- **Pandas** (Manipulação e Análise de Dados)
- **Plotly Express** (Visualizações Gráficas Interativas)
- **Requests** (Consumo de Dados da API)

## 🔧 Como Executar o Projeto Localmente

1. Clone o repositório para sua máquina:
   ```bash
   git clone https://github.com
   ```

2. Entre no diretório do projeto:
   ```bash
   cd dashboard
   ```

3. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```

4. Execute o aplicativo Streamlit:
   ```bash
   streamlit run Dashboard.py
   ```