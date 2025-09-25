# 💰 API REST de Transações Financeiras

Este projeto é uma **API REST** para gerenciamento de transações financeiras, desenvolvida em **Node.js** com **TypeScript** durante o curso de Node.js da Rocketseat.  
A aplicação permite criar, listar, consultar e obter o resumo de transações (créditos e débitos), utilizando cookies para gerenciamento de sessões.

---

## 🚀 Tecnologias

As principais tecnologias e ferramentas utilizadas neste projeto são:

- [Node.js](https://nodejs.org/) – Ambiente de execução
- [Fastify](https://fastify.dev/) – Framework web rápido e eficiente
- [TypeScript](https://www.typescriptlang.org/) – Tipagem estática
- [Knex](https://knexjs.org/) – Query builder para SQL
- [SQLite](https://www.sqlite.org/) – Banco de dados local
- [Zod](https://zod.dev/) – Validação de esquemas
- [Vitest](https://vitest.dev/) – Testes automatizados
- [Supertest](https://github.com/ladjs/supertest) – Testes de integração
- [Postman](https://www.postman.com/) – Teste e consumo da API
- [Render](https://render.com/) – Deploy da aplicação

---

## ⚙️ Funcionalidades

- ✅ **Criar transação:** Registra uma nova transação (crédito ou débito).
- ✅ **Listar transações:** Retorna todas as transações do usuário.
- ✅ **Consultar transação específica:** Obtém os detalhes de uma transação pelo `id`.
- ✅ **Resumo de transações:** Retorna a soma do saldo (créditos – débitos).

---

## 🛠️ Como Executar o Projeto

### 1️⃣ Pré-requisitos
- **Node.js** (v18 ou superior)
- **npm** ou **yarn**

### 2️⃣ Clonar o repositório
```bash
git clone https://github.com/pedrofaleirosss/api-rest-nodejs.git
cd api-rest-nodejs
```

### 3️⃣ Instalar dependências
```bash
npm install
```

### 4️⃣ Configurar variáveis de ambiente
Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo (exemplo):
```
DATABASE_URL="./db/app.db"
PORT=3333
```

### 5️⃣ Executar migrações
```bash
npm run knex migrate:latest
```

### 6️⃣ Rodar em desenvolvimento
```bash
npm run dev
```

### 7️⃣ Rodar os testes
```bash
npm test
```

---

## 🌐 Endpoints

Base URL: `http://localhost:3333`

| Método | Endpoint                | Descrição                       |
|-------|--------------------------|----------------------------------|
| POST  | `/transactions`          | Criar uma nova transação        |
| GET   | `/transactions`          | Listar todas as transações      |
| GET   | `/transactions/:id`      | Buscar uma transação específica |
| GET   | `/transactions/summary`  | Obter o resumo das transações   |

### Exemplo de criação de transação (POST)
```json
{
  "title": "Freelancer",
  "amount": 8000,
  "type": "credit"
}
```

---

## 🧪 Testes Automatizados

Os testes utilizam **Vitest** e **Supertest** para garantir a qualidade da API.  
Os testes cobrem:
- Criação de transações
- Listagem de transações
- Consulta de transação específica
- Resumo das transações

Execute os testes com:
```bash
npm test
```

---

## 📬 Coleção Postman

Uma coleção do **Postman** está disponível no repositório para facilitar os testes:  
[Ignite Node.js API REST.postman_collection.json](./Ignite%20Node.js%20API%20REST.postman_collection.json)

---

## 🌍 Deploy

A aplicação está hospedada no [Render](https://render.com/).  
Basta substituir a variável `{{url}}` da coleção Postman pela URL do deploy para consumir a API em produção.

---

## 👤 Autor

**Pedro Faleiros**  
[GitHub](https://github.com/pedrofaleirosss)
