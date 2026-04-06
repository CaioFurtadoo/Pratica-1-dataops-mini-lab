\# 📊 DataOps Mini Lab

![WhatsApp Image 2026-04-06 at 19 32 53](https://github.com/user-attachments/assets/91c909a6-4c71-4406-baa5-d7b1fb58daf2)


Este projeto é um pipeline de dados simples desenvolvido como parte de um laboratório introdutório de DataOps.



O objetivo é realizar a ingestão de um arquivo CSV contendo pedidos, armazená-los em um banco analítico local (DuckDB) e executar consultas agregadas.



\---



\## 🚀 Tecnologias utilizadas



\- Python 3.11+

\- Pandas

\- DuckDB

\- Git



\---



\## 📁 Estrutura do projeto

dataops-mini-lab/

├── data/

│ ├── raw/

│ │ └── orders\_2026\_03\_23.csv

│ └── curated/

├── ingestion/

│ └── load\_orders.py

├── docs/

├── warehouse/

├── .gitignore

└── README.md

python -m venv .venv

.venv\\Scripts\\activate   # Windows

pip install pandas duckdb

python ingestion/load\_orders.py

Reflexão

1\. Onde está o dado bruto neste projeto?



O dado bruto está no arquivo CSV localizado em data/raw/orders\_2026\_03\_23.csv.



2\. Qual é o papel do script Python no fluxo?



O script Python realiza a ingestão dos dados, lendo o CSV, transformando os tipos das colunas e carregando os dados em um banco DuckDB para consulta.



3\. O que aconteceria se uma coluna do CSV mudasse de nome?



O pipeline quebraria, pois o script depende dos nomes das colunas para fazer os casts e a criação da tabela. Isso geraria erro na execução.



4\. Por que o primeiro commit no Git é importante?



Porque ele registra a versão inicial funcional do projeto, permitindo rastreabilidade, controle de mudanças e rollback no futuro.



5\. O pipeline funciona, mas ele já pode ser considerado confiável para produção?



Não. Ele ainda não possui validações, tratamento de erros robusto, versionamento de dados, monitoramento ou testes, sendo apenas uma versão inicial.

