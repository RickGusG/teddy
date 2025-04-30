# Teddy Test - Full Stack

## Visão Geral
Este projeto é composto por:
- **Frontend:** React + Vite (`teddy-test`)
- **Backend:** NestJS + TypeORM + Postgres + RabbitMQ (`teddy-test-backend`)
- **Mensageria:** RabbitMQ
- **Banco de Dados:** Postgres

## Como rodar tudo com Docker Compose

### Pré-requisitos
- Docker e Docker Compose instalados

### Subindo o sistema
1. Clone o repositório e acesse a raiz do projeto.
2. Execute:
   ```sh
   docker-compose up --build
   ```
3. Acesse os serviços:
   - **Frontend:** [http://localhost:5173](http://localhost:5173)
   - **Backend (API/Swagger):** [http://localhost:3000/api](http://localhost:3000/api)
   - **RabbitMQ UI:** [http://localhost:15672](http://localhost:15672) (user: guest, senha: guest)
   - **Postgres:** localhost:5432 (user: postgres, senha: postgres, db: teddy)

### Variáveis de ambiente
As variáveis já estão configuradas no `docker-compose.yml` para todos os serviços.

## Arquitetura
- **Frontend:** React + Vite
- **Backend:** NestJS, TypeORM, Postgres, RabbitMQ
- **Mensageria:** RabbitMQ para eventos (ex: criação de cliente)
- **Documentação:** Swagger no backend
- **Testes:** Unitários no backend
- **Deploy:** Docker Compose para orquestração

## Instruções locais
Para rodar apenas o backend ou frontend localmente, consulte os READMEs em `teddy-test-backend/` e `teddy-test/`. 