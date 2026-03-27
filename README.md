📄 README.md
# ✈️ Data Warehouse - Companhia Aérea

Projeto de modelagem dimensional (Star Schema) desenvolvido para fins acadêmicos, com foco em análise de dados e Business Intelligence.

---

## 📊 Visão Geral

Este projeto transforma um modelo transacional (OLTP) em um modelo analítico (OLAP), utilizando a abordagem de **Star Schema**.

O objetivo é permitir análises eficientes de:

- Receita
- Ocupação de voos
- Comportamento de clientes
- Impacto de regras tarifárias

---

## 🧠 Modelagem

O modelo foi estruturado com:

### ⭐ Tabela Fato
- `fato_bilhete` → representa a emissão de bilhetes

### 🌟 Dimensões
- `dim_data` (SCD Tipo 0)
- `dim_passageiro` (SCD Tipo 1)
- `dim_tarifa` (SCD Tipo 2)
- `dim_voo`
- `dim_assento`
- `dim_reserva`

---

## 📐 Grão da Fato

> 1 linha representa 1 bilhete emitido por passageiro em um voo instância

---

## 🔑 Conceitos Aplicados

- **Star Schema**
- **Surrogate Keys (SK)**
- **Slowly Changing Dimensions (SCD)**
  - Tipo 0 → imutável
  - Tipo 1 → sobrescrita
  - Tipo 2 → histórico

---

## 📁 Estrutura do Projeto


dw-companhia-aerea/
│
├── docs/
│ └── Entrega_Final_Data_Warehouse.pdf
│
├── sql/
│ └── create_dw.sql
│
├── README.md


---

## 📦 Script SQL

O arquivo `create_dw.sql` contém:

- Criação do schema
- Criação das tabelas fato e dimensões
- Definição de:
  - Primary Keys (PK)
  - Foreign Keys (FK)
  - Constraints

---

## 🚀 Como utilizar

1. Executar o script SQL:
```sql
CREATE SCHEMA schema_dw;
Rodar o arquivo:
create_dw.sql
Utilizar o modelo para análises de BI

📈 Possíveis Análises
Receita por período
Receita por rota
Taxa de ocupação
Ticket médio por cliente
Impacto de mudanças de tarifa
🛠️ Tecnologias

SQL
Modelagem Dimensional
Data Warehouse
Star Schema

👨‍💻 Autor

Arthur Peres

📌 Observação

Este projeto foi desenvolvido para fins acadêmicos, com foco em boas práticas de engenharia de dados e modelagem analítica.
