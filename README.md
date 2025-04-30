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
1. Clone o repositório recursivamente e acesse a raiz do projeto.
   ```sh
   git clone --recursive git@github.com:RickGusG/teddy.git
   ```
2. Execute:
   ```sh
   docker-compose up --build
   ```
3. Acesse os serviços:
   - **Frontend:** [http://localhost:5173](http://localhost:5173)
   - **Backend (API/Swagger):** [http://localhost:3000/api](http://localhost:3000/api)
   - **RabbitMQ UI:** [http://localhost:15672](http://localhost:15672) (user: guest, senha: guest)
   - **Postgres:** [http://localhost:5432](http://localhost:5432) (user: postgres, senha: postgres, db: teddy)

### Variáveis de ambiente
As variáveis já estão configuradas no `docker-compose.yml` para todos os serviços.

## Arquitetura
- **Frontend:** React + Vite
- **Backend:** NestJS, TypeORM, Postgres, RabbitMQ
- **Mensageria:** RabbitMQ para eventos (ex: criação de cliente)
- **Documentação:** Swagger no backend
- **Deploy:** Docker Compose para orquestração

## Instruções locais
Para rodar apenas o backend ou frontend localmente, consulte os READMEs em `teddy-test-backend/` e `teddy-test/`. 

## Q&A desenvolvimento de um painel administrativo
### 1. Quanto tempo levaria?
   - Para um MVP funcional: 2-3 meses
   - Desenvolvimento completo: 4-6 meses
   - Considerando:
     - Desenvolvimento do frontend e backend
     - Testes automatizados
     - Documentação
     - Período de homologação
     - Ajustes e correções
     
### 2. Quantos desenvolvedores?
   - Time mínimo recomendado:
     - 2 desenvolvedores fullstack ou
     - 1 frontend + 1 backend
   - Time ideal:
     - 2-3 desenvolvedores frontend
     - 2 desenvolvedores backend
     - 1 tech lead/arquiteto
     - 1 QA

### 3. Qual a senioridade dos desenvolvedores?
   - Time mínimo:
     - Desenvolvedores fullstack sênior ou
     - 1 frontend pleno/sênior + 1 backend pleno/sênior
   - Time ideal:
     - Frontend: 1 sênior + 1-2 pleno/júnior
     - Backend: 1 sênior + 1 pleno
     - Tech lead/arquiteto sênior
     - QA pleno/sênior