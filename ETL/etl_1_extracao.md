# 🔄 Processo de ELT

## 📌 Visão Geral

O processo de ELT (Extract, Load, Transform) deste projeto foi estruturado com o objetivo de transformar dados não estruturados — originalmente disponibilizados em arquivos PDF — em uma base tabular e pronta para consumo.


---

## 🔍 Etapa 1 — Análise Exploratória dos Dados

O primeiro passo do processo consistiu na identificação do formato dos arquivos disponibilizados no site da TBH Esportes.

Essa análise foi de caráter **exploratório**, com o objetivo de entender:

- Estrutura dos PDFs  
- Padrões de layout das tabelas  
- Tipos de informações disponíveis (nome, tempo, colocação, equipe, etc.)  
- Possíveis variações de dados entre diferentes corridas  

Apesar de superficial neste primeiro momento, essa etapa foi essencial para direcionar as decisões das fases seguintes do pipeline, principalmente no que diz respeito à extração automatizada dos dados.

---

## 📥 Etapa 2 — Extração dos Dados

Os dados foram coletados a partir de todas as corridas realizadas até 03/05/2026. Nesse período, ocorreram 27 corridas, das quais 20 foram efetivamente extraídas, totalizando 117 arquivos obtidos como base inicial do projeto.

O processo de extração contou com o apoio de Inteligência Artificial, responsável pela leitura e extração das informações contidas nos arquivos PDF disponibilizados no site.


### 📁 Padronização de Arquivos

Durante a extração, foi definido um padrão importante para organização dos dados:

- O **nome do arquivo** passou a conter:
  - Nome da corrida  
  - Data de realização
  - Distância percorrida  

**Exemplo do nome do arquivo**:<br> *2026-01-25_Park_Run_2026_06KM-FEMININO-1*

Essa decisão foi necessária porque essas informações **não estão presentes dentro do conteúdo dos arquivos**, sendo fundamentais para contextualização e análises futuras.

---

### ⚠️ Tratamento de Exceções 

Apesar da existência de 27 corridas no período analisado, nem todas puderam ser incluídas na base de dados nesta etapa inicial.
Abaixo estão os casos identificados e seus respectivos motivos:

---

### 📅 Março

- **08/03/2026 — Segunda Corrida Vitoriosa**  
  A corrida está hospedada em outro site, e o destino do redirecionamento não contém os dados da prova.

- **15/03/2026 — 118 Anos | Treinão de Aniversário do Galo**  
  Por se tratar de um evento no formato de treino, não houve mensuração de tempo dos participantes.

- **15/03/2026 — Corrida Divas na Pista 2026**  
    Os dados estão disponíveis em PDF, porém em um formato diferente do padrão encontrado no site TBH Esportes.  
    Essa variação exigirá um tratamento específico, que será abordado em uma segunda etapa do projeto.  

- **22/03/2026 — Centauro Desbrava**  
  A página redireciona para um site promocional sem resultados.  
  Foi identificado um outro domínio contendo os dados, porém em formato HTML, o que exigiria uma abordagem diferente de extração.  
  Para fins deste projeto, optou-se por não incluir neste momento.

- **28/03/2026 — Caminhada Mano Down**  
  Não foi encontrado link com os resultados da corrida.

---

### 📅 Abril

- **26/04/2026 — Corrida Cats Run**  
  Os dados estão disponíveis em PDF, porém em um formato diferente do padrão encontrado no site TBH Esportes.  
  Essa variação exigirá um tratamento específico, que será abordado em uma segunda etapa do projeto.

- **26/04/2026 — Caminhada Holofotes da Inclusão Janaina Barcelos**  
  A página de origem apresenta erro (quebrada), impossibilitando o acesso aos dados.

---

## 🧠 Considerações sobre o Processo

Essas exceções reforçam um ponto importante em projetos reais de dados:

> Nem sempre os dados estão disponíveis de forma padronizada ou acessível.

Durante o desenvolvimento desta pipeline, foi necessário tomar decisões práticas, como:

- Definir escopo inicial de dados 
- Adiar casos mais complexos para etapas futuras  

Essa abordagem permite evolução incremental do projeto, mantendo qualidade e governança sobre os dados já processados.

---

## 🔜 Próximos Passos

Após a etapa de extração e carga dos dados brutos, o pipeline segue para:

- Tratamento e padronização dos dados  
- Criação de camadas analíticas  
- Modelagem para consumo no Power BI  

---