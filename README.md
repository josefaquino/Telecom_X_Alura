# 📊 Análise de Evasão de Clientes (Churn) - Telecom X

Este repositório contém um projeto de Análise de Dados focado em entender e prever a evasão de clientes (churn) em uma empresa de telecomunicações fictícia, a "Telecom X". O objetivo é identificar os principais fatores que levam os clientes a cancelar seus serviços e propor recomendações acionáveis para melhorar a retenção.

---

### 💡 Problema de Negócio

A evasão de clientes (churn) é um desafio crítico para empresas de telecomunicações, impactando diretamente a receita e o crescimento. Entender por que os clientes saem é o primeiro passo para desenvolver estratégias eficazes de retenção e, assim, otimizar os investimentos em aquisição e manutenção de clientes.

---

### 🎯 Objetivo do Projeto

* Realizar uma Análise Exploratória de Dados (EDA) aprofundada para identificar padrões e correlações entre as características dos clientes, os serviços que utilizam e seu status de churn.
* Extrair insights claros e visualmente representados para comunicar descobertas-chave.
* Propor recomendações estratégicas baseadas em dados para a Telecom X reduzir sua taxa de churn.

---

###  metodologia

O projeto seguiu as seguintes etapas:

1.  **Extração de Dados**:
    * Os dados brutos foram obtidos do arquivo `TelecomX_Data.json`.
    * Utilizamos a biblioteca `pandas` para carregar e inspecionar a estrutura inicial do conjunto de dados.

2.  **Transformação e Limpeza de Dados**:
    * **Normalização de Dados Aninhados**: Colunas com estruturas aninhadas (e.g., `customer`, `phone`, `internet`, `account`) foram desdobradas em colunas individuais para facilitar a análise.
    * **Tratamento de Valores Ausentes e Tipos de Dados**: A coluna `TotalCharges` foi convertida para tipo numérico, e seus valores ausentes (que representavam clientes novos sem cobrança total acumulada) foram preenchidos com `0`.
    * **Padronização de Tipos Categóricos**: Colunas com valores discretos (e.g., `Churn`, `gender`, `Contract`) foram convertidas para o tipo `category` do Pandas, otimizando o uso de memória e a performance em análises.
    * **Verificação de Duplicatas**: Foi realizada uma checagem na coluna `customerID` para garantir a unicidade de cada registro de cliente.

3.  **Análise Exploratória de Dados (EDA) e Visualização**:
    * Utilização de `matplotlib` e `seaborn` para criar gráficos descritivos.
    * Análises focadas na relação entre diversas variáveis e o `Churn`, incluindo:
        * Proporção geral de churn.
        * Churn por **Tipo de Contrato** (e.g., mês a mês vs. anuais).
        * Churn por **Serviço de Internet** (e.g., DSL vs. Fibra Óptica).
        * Distribuição de **Despesas Mensais (MonthlyCharges)** entre clientes com e sem churn.
        * Churn entre **Clientes Idosos (SeniorCitizen)**.
        * **[GRÁFICO CHAVE] Churn por Tempo de Contrato (Tenure)**: Esta análise detalhou a distribuição do tempo de permanência do cliente e seu status de churn, revelando picos de evasão em períodos cruciais (como nos primeiros meses de contrato).

---

### 📊 Principais Insights

* **Contratos de Mês a Mês:** Clientes com contratos de "mês a mês" apresentam uma taxa de churn significativamente mais alta, indicando menor lealdade e maior flexibilidade para trocar de serviço.
* **Serviços de Internet:** Clientes com serviço de Fibra Óptica podem ter uma tendência maior a churn, o que sugere possíveis problemas de satisfação ou expectativas em relação a este serviço de alta velocidade.
* **Despesas Mensais:** Clientes com "MonthlyCharges" mais elevadas tendem a churnar mais, possivelmente devido à percepção de custo-benefício.
* **Tempo de Contrato (Tenure):** O **período inicial de um contrato** (primeiros meses) é crítico, com um volume considerável de churn de novos clientes. Além disso, a proximidade do vencimento de contratos mais longos (12 ou 24 meses) também pode ser um gatilho para a evasão.

---

### 📝 Recomendações

Com base nos insights, as seguintes ações são recomendadas para a Telecom X:

1.  **Programas de Fidelização para Clientes Mês a Mês**: Oferecer incentivos, descontos ou benefícios exclusivos para estimular a migração para contratos de longo prazo.
2.  **Melhoria do Onboarding e Suporte Inicial**: Investir na experiência do cliente nos primeiros meses, com acompanhamento proativo, tutoriais claros e um suporte técnico ágil para reduzir o churn precoce.
3.  **Revisão do Serviço de Fibra Óptica**: Conduzir pesquisas de satisfação e analisar feedback de clientes de Fibra Óptica para identificar e corrigir pontos de atrito (e.g., preço, estabilidade, suporte).
4.  **Gestão de Clientes de Alto Valor**: Criar um plano de retenção específico para clientes com "MonthlyCharges" mais altas, garantindo que se sintam valorizados e que suas expectativas sejam atendidas.
5.  **Proatividade na Renovação de Contratos**: Entrar em contato com clientes próximos da renovação de contratos de 12 e 24 meses com ofertas personalizadas ou upgrades para incentivá-los a permanecer.

---

### 🛠️ Tecnologias Utilizadas

* **Python** (Linguagem de Programação)
* **Pandas**: Manipulação e análise de dados.
* **Matplotlib**: Criação de gráficos estáticos.
* **Seaborn**: Visualizações estatísticas atraentes.
