# Order Microservice (order-ms)

## Tech Stack
- **Spring Boot**
- **MongoDB**
- **RabbitMQ**

## Desafio
Construir um microserviço que seja capaz de:
- Processar pedidos a partir de uma fila RabbitMQ.
- Criar uma API Rest que permita consultar:
  - Valor total de um pedido.
  - Quantidade de pedidos por cliente.
  - Lista de pedidos realizados por cliente.

## Configuração da Fila RabbitMQ
- **Nome da fila:** `order-ms`
- **Content-Type:** `application/json`

### Exemplo de Mensagem na Fila
```json
{
  "codigoPedido": 1001,
  "codigoCliente": 1,
  "itens": [
    {
      "produto": "lapis",
      "quantidade": 100,
      "preco": 1.1
    },
    {
      "produto": "caderno",
      "quantidade": 10,
      "preco": 1.0
    }
  ]
}
