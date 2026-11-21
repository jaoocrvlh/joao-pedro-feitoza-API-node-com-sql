# API REST com Node.js, Express e MySQL

**Aluno:** João Pedro Carvalho Feitoza
**Turma:** (preencha sua turma)
**Disciplina:** Programação Web III (PW3) — Trabalho Prático

API REST de CRUD de usuários feita com Express e `mysql2` (pool de conexões), usando SQL direto com queries parametrizadas (`?`) contra SQL Injection, sem ORM.

## Como rodar

1. Instale as dependências:
   ```bash
   npm install
   ```
2. Crie o banco e a tabela executando o `schema.sql` no MySQL:
   ```bash
   mysql -u seu_usuario -p < schema.sql
   ```
3. Copie o `.env.example` para `.env` e preencha com suas credenciais:
   ```bash
   cp .env.example .env
   ```
4. Inicie o servidor:
   ```bash
   npm start
   ```

## Endpoints

| Método | Rota | Descrição |
|--------|------|-----------|
| POST | /usuarios | Cria usuário (`nome`, `email` no body) |
| GET | /usuarios | Lista todos os usuários |
| PUT | /usuarios/:id | Atualiza um usuário |
| DELETE | /usuarios/:id | Remove um usuário |

Exemplo de body (POST/PUT):
```json
{ "nome": "Maria Souza", "email": "maria@exemplo.com" }
```
