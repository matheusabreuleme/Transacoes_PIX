# Case Transações PIX
## Análise de Transações PIX

### Objetivos
- Limpar e pré-processar os dados das transações PIX
- Analisar padrões de uso do PIX, tais como os canais mais utilizados e os valores de transação mais comuns
- Use o PySpark MLlib para treinar e avaliar um modelo de detecção de fraude
- Avaliar o desempenho do modelo e fazer recomendações para melhorias futuras

### Dados

O conjunto de dados inclui as seguintes informações para cada transação:
- Detalhes da transação: valor, tempo, remetente e receptor CPF/CNPJ, tipo
- Etiqueta de fraude: uma variável binária que indica se a transação foi fraudulenta (1) ou não (0)

### Tarefas
- Normalização dos dados:
  - O dataset está em formato json.
  ```json
  {
      "id_transacao": inteiro,
      "valor": texto,
      "remetente": {
          "nome": texto,
          "banco": texto,
          "tipo": texto
      }, 
      "destinatario": {
          "nome": texto, 
          "banco":texto,
          "tipo": texto
      },          
      "categoria":texto,
      "chave_pix":texto,
      "transaction_date":texto,
      "fraude":inteiro,
  }
    ```


# Entendimento do Negócio
Você trabalha em um banco e o principal meio de pagamento utilizado no seu banco é o Pix. 

Através da base de transações do pix o banco deseja entender qual é o perfil dos clientes que utilizam o pix, além de verificar possíveis transações que tenham fraude. Porém, eles tem um cliente específico que tem um relacionamento muito bom para o banco, por isso, você recebeu a base de transações de cliente dos últimos 2 anos e precisa a partir dela criar um relatório contendo as principais características das transações. 
