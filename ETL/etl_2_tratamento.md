# 🔍 Etapa 3 — Tratamento dos Dados

Para este projeto, foi estruturado um Data Lakehouse seguindo o padrão da Arquitetura Medalhão (Medallion Architecture), amplamente utilizada em pipelines modernos de dados.

O Amazon S3 (AWS) foi utilizado para hospedar a Camada Bronze. Nesta etapa, os arquivos são armazenados em seu formato original (raw data), garantindo a preservação da 'fonte da verdade' e possibilitando reprocessamentos, auditorias e futuras transformações sem perda de integridade.

Essa abordagem assegura alta confiabilidade, rastreabilidade e flexibilidade ao longo de todo o ciclo de vida dos dados.

![alt text](medallion_architecture-1.png)

Com os dados armazenados na camada Bronze, foi desenvolvido um script em Python, com apoio de Inteligência Artificial (IA), para realizar a extração das informações contidas em arquivos no formato PDF e sua conversão para o formato Parquet, estruturado e otimizado para dados tabulares.

Para a execução desse processo de transformação, foi utilizado o Google Colab. Ao final da etapa, os dados já estruturados foram carregados em um novo bucket no Amazon S3, representando a camada Silver da arquitetura.


-------

### 🚦 Desafios


> "A inteligência artificial é a nova eletricidade, mas ainda precisamos de humanos para decidir como usá-la." — Andrew Ng

O uso da Inteligência Artificial até este momento do projeto foi essencial, pois viabilizou a extração automatizada dos dados e apoiou na criação de scripts em Python, linguagem na qual ainda estou em desenvolvimento. Sua utilização agregou agilidade ao processo e contribuiu para a evolução técnica ao longo do projeto.

No entanto, o uso isolado da IA não é suficiente para gerar valor. É fundamental que haja análise crítica e compreensão dos resultados obtidos, garantindo que as informações sejam interpretadas de forma correta e aplicada de maneira estratégica.

Dessa forma, utilizar IA sem o devido entendimento dos resultados limita seu potencial e pode comprometer a qualidade das entregas.

**Diferença entre os cabeçalhos**

O primeiro desafio encontrado foi a padronização das colunas dos arquivos. Entre os 117 arquivos armazenados no S3, foram identificados três diferentes formatos, sendo eles:

>=== Tipo 1 (108 arquivos) === <br>
>('Coloc.', 'Num.', 'Nome', 'Sx.', 'Idd.', 'Faixa', 'Cl.Fx.', 'Equipe', 'Tempo', 'Liquido')

>=== Tipo 2 (2 arquivos) === <br>
('Coloc.', **'Numero'**, 'Nome', 'Sx.',**'Id.'**, **'Fx.Et.'**, 'Cl.Fx.', **'C.'**, 'Equipe', 'Tempo')

>=== Tipo 3 (3 arquivos) === <br>
('Coloc.', 'Número', 'Nome', **'Id.'**, 'Faixa', **'C.F.'**, 'Equipe', **'Corrida'**, **'Ciclismo'**, **'Corrida'**, 'Tempo')

