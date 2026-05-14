# Projeto Apache Hop — Primeiros Passos

## 👥 Dupla
- Victor Macedo Cruz Belo  
- Felipe Gabriel Loose  

---

## 📌 Descrição

Este projeto foi desenvolvido com base na atividade proposta no seguinte repositório:

https://github.com/tharlisdavid/primeiros-passos-apache-hop/tree/main

O objetivo é praticar a criação de pipelines ETL utilizando o Apache Hop, realizando integração de dados entre tabelas de vendas, produtos e vendedores em um banco PostgreSQL, com carga final em uma tabela de Data Warehouse.

---

## ⚙️ Tecnologias utilizadas

- Apache Hop Web
- PostgreSQL 15
- pgAdmin
- Docker Compose
- Git e GitHub

---

## 🧱 Estrutura do ambiente

O ambiente foi construído utilizando Docker Compose, contendo:

- Apache Hop Web (http://localhost:8080/ui)
- PostgreSQL (porta 5432)
- pgAdmin (http://localhost:5050)

---

## 🔗 Pipeline ETL

O pipeline desenvolvido realiza:

- Leitura das tabelas:
  - vendas
  - produtos
  - vendedor

- Integração dos dados utilizando Merge Join
- Transformações e cálculos (ex: quantidade × valor)
- Padronização de colunas
- Carga final na tabela `dw_vendas`

---

## 🗄️ Banco de dados

Banco utilizado: `hopdb`

### Tabelas de origem:
- produtos
- vendedor
- vendas

### Tabela destino:
- dw_vendas (Data Warehouse)

---

### Como executar o projeto
-- 1. Subir o ambiente com Docker
`docker-compose up -d`


-- 2. Acessar os serviços
Apache Hop Web: http://localhost:8080/ui
pgAdmin: http://localhost:5050

-- 3. Executar o pipeline
Abra o Apache Hop Web e execute o pipeline:
filename.hpl

---

Resultado final

O pipeline gera uma tabela consolidada de vendas contendo:

- Data da venda
- Nome do produto
- Nome do vendedor
- Quantidade vendida
- Valor total calculado
