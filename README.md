# Pipeline ETL de Extração de Preço do Bitcoin via API Coinbase

Este projeto realiza a extração automática do preço do Bitcoin utilizando a API pública da Coinbase, transforma os dados e armazena localmente em um banco de dados leve (TinyDB).

## Como funciona

1. **Extração (Extract):**
   - A função `extrair()` faz uma requisição HTTP para a API da Coinbase e obtém o preço atual do Bitcoin.

2. **Transformação (Transform):**
   - A função `transformar(dados_json)` recebe a resposta da API, extrai os campos relevantes (valor, criptomoeda, moeda) e adiciona um timestamp.

3. **Carga (Load):**
   - A função `load(dados_tratados)` insere os dados tratados em um banco TinyDB chamado `db.json`.

4. **Execução contínua:**
   - O bloco principal executa o processo ETL em loop, coletando e armazenando os dados a cada 5 segundos.

## Requisitos

- Python 3.x
- requests
- tinydb

Instale as dependências com:
```bash
pip install requests tinydb
>>>>>>> Stashed changes
