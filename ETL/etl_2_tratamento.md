# 🔍 Etapa 3 — Tratamento dos Dados

Para este projeto, foi estruturado um Data Lakehouse, seguindo o padrão da Arquitetura Medalhão (Medallion Architecture), amplamente utilizada em pipelines modernos de dados.

A camada de staging é representada pelo Amazon S3 (AWS), atuando como a camada Bronze. Nessa etapa, os dados são armazenados em seu formato bruto (raw data), garantindo a preservação das informações originais e possibilitando reprocessamentos, auditorias e futuras transformações.

Essa abordagem assegura maior confiabilidade, rastreabilidade e flexibilidade ao longo de todo o pipeline de dados.


![alt text](medallion_architecture-1.png)