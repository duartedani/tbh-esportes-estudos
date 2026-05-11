# 🔄 Processo de ELT

---

## 🎯 Objetivo da Análise

Antes de iniciar qualquer etapa técnica, é fundamental definir o objetivo da análise.<br>
Fazendo um paralelo com a área de negócio, essa etapa responde à seguinte pergunta:

> **Qual problema eu quero resolver com esses dados?**

Ou, de forma mais ampla:

> *"Se você não sabe para onde quer ir, qualquer caminho serve."*

Essa definição é essencial, pois orienta todas as decisões ao longo do pipeline — desde a extração até a modelagem e visualização dos dados.

---

### 💡 Contexto do Projeto

Este projeto nasceu a partir de um interesse pessoal: entender meu desempenho em corridas ao longo do ano de **2025** e compará-lo com o ano de **2026**.

A partir desse objetivo inicial, a análise foi expandida com uma nova perspectiva:

- Como esses dados poderiam ser utilizados por uma **assessoria de corrida** para acompanhar e melhorar o desempenho de seus atletas?

Com isso, o projeto evoluiu de uma análise individual para uma abordagem mais ampla, explorando possibilidades como:

- Monitoramento de performance ao longo do tempo  
- Identificação de evolução ou queda de rendimento  
- Comparações entre atletas  
- Geração de insights para tomada de decisão  

Essa expansão permitiu transformar um interesse pessoal em um **projeto estruturado de análise de dados**, com aplicação prática no contexto esportivo.

---


## 📦 Escopo do Projeto

Devido à magnitude e diversidade de analises que esses dados oferecem, o projeto foi estruturado em etapas, permitindo uma evolução incremental e controlada do pipeline.

---

### 🥇 Etapa 1 — Construção da Pipeline (Base 2026)

A primeira etapa consiste na construção completa da pipeline de dados utilizando exclusivamente os dados do ano de **2026**.

A escolha por essa base se deve ao seu menor volume, permitindo sua utilização como ambiente de teste e validação.

Nesta fase, estão contempladas as seguintes atividades:

- Identificação e análise dos dados  
- Extração das informações  
- Modelagem dos dados  
- Estruturação da base analítica  
- Construção de dashboard  

---

### 🥈 Etapa 2 — Expansão para Dados de 2025

Com os aprendizados obtidos na etapa anterior, será realizado o tratamento e estruturação dos dados referentes ao ano de **2025**.

---

### 🥉 Etapa 3 — Análise Comparativa

Na etapa final, será realizada a integração das bases de **2025** e **2026**, possibilitando análises comparativas.


---

## ⚙️ Etapas Pós-Extração

Após a extração e carga dos dados brutos, o pipeline segue para as etapas de:

- Tratamento e padronização dos dados  
- Modelagem da base analítica  

É a partir desse ponto que os dados passam a estar prontos para geração de valor através da análise.

---

## 📊 Camadas de Análise

A análise será conduzida a partir de duas visões principais:

---

### 👟 Visão do Corredor

Focada na análise individual do atleta, permitindo:

- Acompanhamento da evolução de performance  
- Comparação de tempos entre provas  
- Frequência de participação em corridas  
- Análise de ritmo (pace)  
- Histórico esportivo ao longo do tempo  

---

### 🧑‍🏫 Visão da Assessoria de Corrida

Voltada para uma análise mais estratégica, permitindo que assessorias esportivas:

- Monitorem o desempenho de seus atletas  
- Identifiquem padrões de evolução ou queda de performance  
- Comparem atletas entre si  
- Acompanhem participação em eventos  
- Gerem insights para melhoria de desempenho  
- Apoiem decisões técnicas com base em dados  

---