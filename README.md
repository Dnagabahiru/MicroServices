## Microservices Architecture Diagram

```
                CLIENT / FRONTEND
                 (Web / Mobile)
                        |
                        v
                 -----------------
                 |   API GATEWAY |
                 | Auth • Routing|
                 | Rate Limiting |
                 -----------------
                        |
        -----------------------------------------
        |                   |                   |
        v                   v                   v

   -------------      -------------      -------------
   | USER      |      | ORDER     |      | PAYMENT   |
   | SERVICE   |      | SERVICE   |      | SERVICE   |
   | SpringBoot|      | SpringBoot|      | SpringBoot|
   -------------      -------------      -------------
        |                   |                   |
        v                   v                   v

    -----------        -----------        -----------
    | User DB |        | Order DB|        |Payment DB|
    -----------        -----------        -----------

            \             |             /
             \            |            /
              \           |           /
               v          v          v

                -----------------------
                |   MESSAGE BROKER    |
                |  Kafka / RabbitMQ   |
                -----------------------
                          |
                          v
                -----------------------
                | MONITORING & LOGGING|
                | Prometheus • Grafana|
                | ELK Stack           |
                -----------------------
```
