# 📊 Análise Socioeconômica do Desempenho no ENEM com Machine Learning

Este projeto investiga como **fatores socioeconômicos, demográficos e
escolares influenciam o desempenho de estudantes no ENEM** utilizando
técnicas de **Machine Learning**.

A partir dos **microdados do ENEM 2018**, foram construídos modelos
capazes de **estimar a nota média de um candidato** com base apenas em
informações socioeconômicas, sem utilizar diretamente seu histórico
pedagógico.

O projeto foi desenvolvido como parte da disciplina de **Aprendizado de
Máquina da Universidade Federal do Ceará (UFC)**.

------------------------------------------------------------------------

# 🎯 Objetivo

O objetivo principal deste projeto é:

-   Construir modelos de **regressão capazes de prever a nota média do
    ENEM**
-   Investigar **o impacto de variáveis socioeconômicas no desempenho
    acadêmico**
-   Comparar diferentes algoritmos de **Machine Learning**
-   Demonstrar como **dados educacionais podem revelar padrões sociais
    relevantes**

------------------------------------------------------------------------

# 📂 Base de Dados

Foram utilizados os **microdados do ENEM 2018**, disponibilizados
publicamente pelo INEP.

Após o processo de filtragem e limpeza, o dataset final possui
aproximadamente:

-   **289 mil candidatos**
-   **40 variáveis socioeconômicas**
-   variável alvo: **nota média do candidato no ENEM**

As variáveis incluem informações como:

-   renda familiar
-   escolaridade dos pais
-   tipo de escola
-   acesso a computador e internet
-   características demográficas

------------------------------------------------------------------------

# ⚙️ Pipeline do Projeto

O projeto segue um pipeline completo de **Ciência de Dados e Machine
Learning**.

## 1️⃣ Seleção das Variáveis

Inicialmente foram selecionadas variáveis relevantes relacionadas a:

-   características demográficas
-   informações educacionais
-   fatores socioeconômicos

Variáveis diretamente ligadas às notas individuais foram removidas para
evitar **data leakage**.

------------------------------------------------------------------------

## 2️⃣ Pré-processamento dos Dados

Os microdados do ENEM são extensos e possuem diversas inconsistências,
exigindo um processo cuidadoso de preparação.

As principais etapas foram:

### Limpeza dos dados

-   Remoção de candidatos ausentes nas provas
-   Remoção de registros incompletos
-   Tratamento de valores nulos

### Seleção de participantes válidos

Foram mantidos apenas candidatos que:

-   realizaram todas as provas
-   possuem dados socioeconômicos completos

### Conversão de formatos

Os dados foram convertidos para **Parquet**, um formato colunar
eficiente que:

-   reduz espaço em disco
-   acelera leitura e processamento
-   melhora performance em datasets grandes

### Tratamento de variáveis categóricas

Variáveis categóricas foram tratadas utilizando:

-   codificação apropriada para modelos de árvore
-   transformação para formatos compatíveis com bibliotecas de ML

------------------------------------------------------------------------

# 📈 Modelagem

Foram testados diferentes algoritmos de regressão para estimar a nota
média.

Os modelos avaliados foram:

-   **Regressão Linear**
-   **Random Forest**
-   **LightGBM**
-   **CatBoost**

Cada modelo foi treinado utilizando **divisão treino-teste** do dataset.

------------------------------------------------------------------------

# 📏 Métricas de Avaliação

Os modelos foram avaliados utilizando métricas padrão para regressão:

### MAE (Mean Absolute Error)

Mede o erro médio absoluto entre as notas previstas e as reais.

### RMSE (Root Mean Squared Error)

Penaliza erros maiores de forma mais severa.

### R² (Coeficiente de Determinação)

Indica o quanto da variabilidade dos dados é explicada pelo modelo.

------------------------------------------------------------------------

# 🏆 Resultados

O modelo com melhor desempenho foi:

**CatBoost Regressor**

Resultados aproximados:

-   **MAE:** 58.30 pontos
-   **R²:** \~0.38

Esses resultados mostram que **fatores socioeconômicos possuem
influência significativa no desempenho no ENEM**, mas não explicam
totalmente as notas dos estudantes.

------------------------------------------------------------------------

# 💡 Principais Insights

A análise revelou que variáveis como:

-   renda familiar
-   acesso a tecnologia
-   tipo de escola
-   escolaridade dos pais

estão entre os fatores mais associados ao desempenho no exame.

Ao mesmo tempo, os resultados indicam que **essas variáveis não
determinam completamente o resultado de um estudante**, mostrando que
outros fatores também desempenham papel importante.

------------------------------------------------------------------------

# 🛠️ Tecnologias Utilizadas

-   **Python**
-   **Polars**
-   **Pandas**
-   **Scikit-learn**
-   **LightGBM**
-   **CatBoost**

------------------------------------------------------------------------

# 👥 Autores

Projeto desenvolvido por:

-   **Andrey Henrique**
-   **Paulo Jânio**
-   **Clara Aguiar**

Universidade Federal do Ceará --- UFC

------------------------------------------------------------------------

# 📌 Possíveis Melhorias Futuras

Algumas extensões possíveis do projeto incluem:

-   utilização de **técnicas de interpretabilidade (SHAP)**
-   análise de **importância das variáveis**
-   experimentos com **redes neurais**
-   análise comparativa com **outros anos do ENEM**
