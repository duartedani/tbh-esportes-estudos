# 🔍 Etapa 3 — Tratamento dos Dados

Para este projeto, foi estruturado um Data Lakehouse seguindo o padrão da Arquitetura Medalhão (Medallion Architecture), amplamente utilizada em pipelines modernos de dados.

O Amazon S3 (AWS) foi utilizado para hospedar a Camada Bronze. Nesta etapa, os arquivos são armazenados em seu formato original (raw data), garantindo a preservação da 'fonte da verdade' e possibilitando reprocessamentos, auditorias e futuras transformações sem perda de integridade.

Essa abordagem assegura alta confiabilidade, rastreabilidade e flexibilidade ao longo de todo o ciclo de vida dos dados.


![alt text](medallion_architecture-1.png)

-------