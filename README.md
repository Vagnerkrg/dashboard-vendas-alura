# 🛒 Dashboard de Vendas com Streamlit

`🐍 Python` `📦 v1.0.0`

🔗 **Acesse o dashboard online:** [projeto-dashboard.streamlit.app](https://projeto-dashboard.streamlit.app/)

Este é um projeto de um painel interativo de vendas desenvolvido em Python utilizando a biblioteca **Streamlit**...

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

   ## ⚠️ Desafios Técnicos e Erros de Deploy Superados

Para colocar este dashboard 100% online e funcional na nuvem do Streamlit, foi necessário diagnosticar e corrigir uma série de erros críticos de infraestrutura e ambiente de produção:

- **Incompatibilidade Binária (`ValueError: numpy.dtype size changed`)**: Correção de conflito de ambiente onde o `pandas` exigia uma versão mais atualizada e estável do `numpy` do que a instalada por padrão.
- **Falta de Dependência Principal (`Error installing requirements`)**: O servidor recusava a inicialização por falta da declaração explícita da biblioteca principal do `streamlit` no arquivo de requerimentos.
- **Instabilidade de API Externa (`HTTP 502 Bad Gateway`)**: Tratamento robusto de exceções com `try/except` e travas de segurança com `st.stop()`, impedindo o travamento completo da tela caso a API de origem fique fora do ar.
- **Incompatibilidade de Versões do Python (Preview vs Stable)**: Correção de quebra de deploy gerada pelo uso de uma versão de testes muito recente (Python 3.14). O ambiente foi corrigido ao migrar o container para o **Python 3.12 estável**.
- **Arquivos fora da Raiz do Repositório Git**: Reorganização da arquitetura de pastas, movendo o arquivo `requirements.txt` diretamente para a raiz (*root*) do repositório, permitindo a instalação correta dos pacotes após forçar a limpeza de cache profunda do container (`Clear cache and deploy`).
