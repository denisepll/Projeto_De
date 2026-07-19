# Projeto_De - Sistema de predição de falhas industriais

*Sobre o projeto*
Este repositório contém o projeto avaliativo final do curso de Desenvolvimento de IA para Análise Preditiva - SCTEC: Pipeline preditivo aplicado a indústria 4.0.

*Objetivo*
O objetivo deste sistema é analisar dados de sensores de máquinas para prever quando um equipamento vai falhar, ajudando a evitar paradas na produção.

## O que o sistema resolve?

Este sistema foi desenvolvido para avisar antecipadamente a equipe de produção que a máquina está em ponto de falha, permitindo que a equipe aplique medidas corretivas em tempo. O problema que ele resolve, portanto, é evitar que a máquina quebre de surpresa e a produção pare, levando a prejuízos com manutenção corretiva e perda de produtividade.

## Vídeo de demonstração


## Estrutura do sistema

Projeto_De
│
├── data/                           
│   ├── docs/                                      # Dados adicionais
│   ├── processed                                  # Dados sintéticos gerados
│   ├── raw/                                       # Dados originais
│
├── notebooks/                                     
│   ├── projeto_final_predicao_falhas.ipynb /      # Arquivo principal = pipeline preditivo
|
├── outputs                                        # Saidas geradas pelo código
|
├── src/                            
│   ├── config.py                                  # Configurações iniciais para os notebooks
│
├── .gitignore                                     # Proteção de arquivos 
└── README.md                                      # Documentação do projeto
├── requirements.txt                               # Bibliotecas necessárias 



## Técnicas e tecnologias utilizadas

O sistema foi construído no VS Code, usando a linguagem Python, dentro de um único notebook Jupyter, dividido nas fases:

1. **Análise exploratória:** Inspeção do dataset, com análise gráfica da distribuição, balanceamento e correlação dos dados.
2. **Limpeza de tratamento dos dados:** Remoção de duplicadas, imputação de valores nulos e identificação de outliers.
3. **Feature engineering:** Criação de uma nova coluna com a potência calculada para ajustar os modelos.
4. **Divisão e balanceamento dos dados:** Separação das variáveis, divisão dos dados para treino e teste e prevenção de vazamento de dados (Data Leakege).
5. **Escalonamento de variáveis:** Aplicação do StandardScaler para ajuste dos dados destinados ao modelo KNN.
6. **Ajuste de parâmetros e combate ao overfitting:** Treinamento dos modelos de Machine Learning KNN e Árvore de decisão através de laços de repetição para testar diferentes configurações e evitar o overfitting.
7. **Avaliação da acurácia e veredito final:** Análise da acurácia final e escolha do modelo com melhor desempenho.

### Bibliotecas utilizadas
* Pandas e Numpy (para carregar e limpar o dataset)
* Matplotlib e Seaborn (para geração dos gráficos)
* Scikit-Learn (para os modelos de Machine Learning)

## Como executar o sistema
Abra o seu terminal de preferência e execute os comandos para baixar o projeto e abri-lo diretamente no VS Code:

### 1. Clonar o repositório
git clone git@github.com:denisepll/Projeto_De.git 
ou 
git clone https://github.com/denisepll/Projeto_De.git

### 2. Instalar o ambiente virtual .venv
python -m venv .venv

### 3. Instalar as Bibliotecas Necessárias
pip install -r requirements.txt

### 4. Abrir e executar o código 
Abra o arquivo localizado em "notebooks/projeto_final_predicao_falhas.ipynb"
Selecione o kernel ".venv" no topo do arquivo e clique no botão "Run All" (executar tudo).


