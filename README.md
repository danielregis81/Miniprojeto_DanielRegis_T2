# 📊 Miniprojeto - Análise Exploratória de Dados de Varejo

**Autor:** Daniel Regis — Turma 2  
**Disciplina:** Projeto III — Análise Exploratória de Dados Utilizando Python

---

## 📝 Descrição do Projeto

Este projeto realiza uma Análise Exploratória de Dados (AED) sobre uma base de vendas de uma rede de supermercados. A base contém **830.000 registros** de compras realizadas por **1.000 clientes** no período de **2010 a 2022**, obtida na plataforma Kaggle.

O objetivo é transformar dados brutos em informações úteis para tomada de decisão, passando por etapas de importação, limpeza, transformação e visualização dos dados.

---

## 📁 Estrutura do Projeto

```
Miniprojeto_DanielRegis_T2/
├── database/
│   ├── Base Varejo.csv          # Base de dados original (Kaggle)
│   ├── df_limpo.csv             # Base tratada e limpa (gerada pelo notebook)
│   └── Projeto III - ...pdf     # Enunciado do projeto
├── Miniprojeto_Varejo_AED.ipynb # Notebook principal com toda a análise
└── README.md                    # Este arquivo
```

---

## 🗂️ Dicionário de Dados

| Coluna     | Descrição                                      |
|------------|------------------------------------------------|
| DATA       | Data da compra                                 |
| CO_ID      | Número da nota fiscal (identificação da compra)|
| CL_ID      | Identificação do cliente                       |
| CL_GENERO  | Sexo biológico (M / F)                         |
| CL_EC      | Estado civil (Casado, Divorciado, Separado, Solteiro, Viúvo) |
| CL_FHL     | Número de filhos do cliente (0 a 4)            |
| CL_SEG     | Segmentação econômica (A, B ou C)              |
| PR_ID      | Código do produto (SKU)                        |
| PR_CAT     | Categoria do produto (Alimentos, Bebidas, Higiene, Limpeza, Acessórios, Pet, Sem Categoria) |
| PR_NOME    | Nome do produto adquirido                      |

---

## 🚀 Como Usar

### Pré-requisitos

- Python 3.10+
- Bibliotecas necessárias:
  - `pandas`
  - `matplotlib`
  - `seaborn`

Instale as dependências com:

```bash
pip install pandas matplotlib seaborn
```

### Execução

1. Clone o repositório ou baixe os arquivos.
2. Abra o notebook `Miniprojeto_Varejo_AED.ipynb` no **VS Code**, **Jupyter Notebook** ou **Google Colab**.
3. Execute as células na ordem sequencial (de cima para baixo).
4. O notebook irá:
   - Importar a base original (`Base Varejo.csv`)
   - Realizar a limpeza e transformação dos dados
   - Salvar a base limpa em `database/df_limpo.csv`
   - Gerar estatísticas descritivas e visualizações

### Possíveis Problemas

- Se ocorrer erro ao acessar `.dt.month` ou `.dt.year`, re-execute a célula que converte a coluna `DATA` para `datetime`.
- Certifique-se de que o arquivo `Base Varejo.csv` está na pasta `database/`.

---

## 🔧 Etapas do Projeto (Sprints)

| Sprint | Tema | Descrição |
|--------|------|-----------|
| 1 | Importação dos Dados | Importação do CSV da plataforma Kaggle para o ambiente de desenvolvimento |
| 2 | Transformação de Tipos | Conversão de strings, inteiros, floats e datetime |
| 3 | Limpeza de Nulos e Duplicatas | Remoção de colunas vazias, tratamento de `#N/D`, eliminação de 96.553 linhas duplicadas |
| 4 | Estatística Descritiva | Cálculo de média, mediana, moda, desvio padrão e geração de gráficos |
| 5 e 6 | Relatório e Documentação | Construção do relatório final e documentação do projeto |

---

## 💡 Principais Insights

### 1. Foco em Alimentos
A maior parte das vendas concentra-se na categoria **Alimentos**, indicando que os clientes priorizam itens essenciais e compram com alta frequência. Isso reforça a importância de manter estoque robusto nessa categoria.

### 2. Segmentação por Perfil (Estado Civil)
Clientes **casados** tendem a comprar significativamente mais itens para casa. Esse comportamento abre oportunidade para campanhas de marketing mais direcionadas a esse público.

### 3. Mix de Produtos
O ranking de vendas por categoria e produto permite identificar rapidamente o que gera mais faturamento, facilitando decisões sobre promoções e reposição de estoque.

### 4. Distribuição de Filhos
- A maioria dos clientes **não tem filhos** (mediana = 0, moda = 0)
- A média é de ~1,15 filhos por cliente
- Clientes com filhos apresentam padrões de compra diferenciados

### 5. Perfil Demográfico
- A distribuição entre gêneros (M/F) é relativamente equilibrada
- O estado civil influencia diretamente o volume e tipo de compras realizadas

### 6. Top 3 Categorias Mais Vendidas
As três categorias com maior volume de transações são: **Alimentos**, **Bebidas** e **Higiene** — todas ligadas ao consumo diário.

---

## ⚠️ Problemas Identificados na Base

| Problema | Impacto |
|----------|---------|
| Dados marcados como `#N/D` na categoria | Prejudica a análise de mercado por categoria |
| Alta quantidade de duplicatas (96.553 linhas) | Pode enviesar resultados se não tratado |
| Ausência de dados de valor/preço | Impossibilita análise de faturamento real |
| Falta de histórico temporal detalhado | Dificulta análise de sazonalidade e previsões |

---

## 📈 Visualizações Geradas

- Distribuição do número de filhos (`CL_FHL`)
- Volume médio de compras por número de filhos
- Top 3 categorias mais vendidas
- Distribuição por gênero (`CL_GENERO`)
- Distribuição por estado civil (`CL_EC`)

---

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Pandas** — manipulação e limpeza de dados
- **Matplotlib** — visualizações gráficas
- **Seaborn** — gráficos estatísticos
- **Jupyter Notebook** — ambiente de desenvolvimento interativo

---

## 📌 Observações Finais

O objetivo deste projeto não é apenas gerar números, mas preparar os dados para que a análise seja confiável. Quando a base está limpa e bem estruturada, as visualizações funcionam melhor e os resultados se tornam mais úteis para decisões de negócio. 
Um agradecimento especial à professora Amanda que tem sido uma ótima guia nessa nova jornada para todos os estudantes da turma T2

---

## 🔗 Fonte dos Dados

[Base Varejo — Kaggle](https://www.kaggle.com/datasets/namespaiva/base-varejo?resource=download)
