# Engenharia e Higienização de Dados de Inventário Global (Excel & Power Query)

### 📌 Cenário de Negócio

Este projeto simula um desafio real de auditoria de estoque internacional. O relatório original (extraído do sistema legado da empresa) continha inconsistências graves: nomes de países sem padronização, colunas com cálculos estáticos desnecessários, chaves misturadas e linhas nulas que quebravam as análises gerenciais.

O objetivo deste projeto foi aplicar o processo de **ETL (Extração, Transformação e Carga)** utilizando o **Power Query** no Excel para higienizar a base e deixá-la pronta para o carregamento em um Data Warehouse ou ferramenta de BI.

### ⚙️ Etapas Aplicadas no Power Query (Lógica de ETL)

1. Padronização de Chaves (Campos de Texto): Mesclagem e tratamento das colunas de Produto e Marca para criação de descritivos únicos e limpos de caracteres especiais.

2. Normalização de Dados Geográficos: Conversão de nomes extensos de países (ex: "Estados Unidos", "China") para o padrão internacional de siglas ISO (US, CH, BR, AR), facilitando futuras junções de tabelas.

3. Otimização de Performance da Base: Eliminação de colunas de subtotal calculadas na origem. A lógica matemática foi removida da tabela física para ser processada em tempo de execução via Dax ou SQL.

4. Remoção de Ruídos: Filtragem de linhas corrompidas e registros totalmente nulos (`null`) gerados por falhas de exportação do sistema anterior.

### 📊 Estrutura Comparativa dos Dados

* Base Bruta (Input):** Dados desalinhados, excesso de colunas redundantes e falta de padronização internacional.

* Base Higienizada (Output):** Dados tipados corretamente, prontos para modelagem dimensional (Star Schema) e criação de dashboards eficientes.

### 🛠️ Tecnologias Utilizadas

**Power Query** (Mecanismo de Transformação de Dados).

**Microsoft Excel** (Armazenamento e Tabelas Dinâmicas).

### 📊 Prints da Planilha:

<img width="1919" height="1079" alt="Captura estoque 01" src="https://github.com/user-attachments/assets/0d82f889-937a-42c0-ac98-f07eb5e7622e" />

<img width="1919" height="1079" alt="Captura estoque 02" src="https://github.com/user-attachments/assets/7744c8c4-6f5d-47cc-9454-fe8ba79a5a91" />

<img width="1919" height="1079" alt="Captura estoque 03" src="https://github.com/user-attachments/assets/8b91734f-da1b-409b-ac62-eff5cbd63363" />


