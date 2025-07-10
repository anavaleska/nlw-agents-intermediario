# NLW Agents

Projeto desenvolvido durante a 20ª Edição da NLW, um evento da Rocketseat.

## BACKEND

### 🚀 Tecnologias

- **Node.js** com TypeScript nativo (experimental strip types)
- **Fastify** - Framework web rápido e eficiente
- **PostgreSQL** com extensão **pgvector** para vetores
- **Drizzle ORM** - Type-safe database operations
- **Zod** - Schema validation
- **Docker** - Containerização do banco de dados
- **Biome** - Linting e formatação de código

<br/>

### 📂 Arquitetura

- **Layered Structure** - Separação de responsabilidades entre rotas, validações e acesso ao banco de dados
- **Schema Validation** - Validação declarativa com Zod para garantir type safety
- **Type-safe ORM** – Integração com banco de dados usando Drizzle com segurança de tipos
- **Environment Validation** – Validação centralizada de variáveis de ambiente com Zod

<br/>

### ⚙️ Configuração do Projeto

### Pré-requisitos

- Node.js (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose
- npm ou yarn

### Instalação

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd <nome-do-repositorio>
cd server
```

### 2. Configure o banco de dados

```bash
docker-compose up -d
```

### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

### 4. Instale as dependências

```bash
npm install
```

### 5. Execute as migrações do banco

```bash
npx drizzle-kit migrate
```

### 6. (Opcional) Popule o banco com dados de exemplo

```bash
npm run db:seed
```

### 7. Execute o projeto

**Desenvolvimento:**

```bash
npm run dev
```

**Produção:**

```bash
npm start
```

## 📚 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo de desenvolvimento com hot reload
- `npm start` - Executa o servidor em modo de produção
- `npm run db:seed` - Popula o banco de dados com dados de exemplo

## 🌐 Endpoints

A API estará disponível em `http://localhost:3333`

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

---

<br>
<br>

## FRONTEND

## 🚀 Tecnologias:

- **React** - Biblioteca para interfaces de usuário
- **TypeScript** - Superset JavaScript com tipagem estática
- **Vite** - Build tool e servidor de desenvolvimento
- **TailwindCSS** - Framework CSS utility-first
- **React Router Dom** - Biblioteca de roteamento
- **TanStack React Query** - Gerenciamento de estado servidor e cache
- **Radix UI** - Componentes primitivos acessíveis
- **Shadcn/ui** - Sistema de componentes
- **Lucide React** - Biblioteca de ícones

<BR>

## 📂 Arquitetura:

- **Component-based Architecture** - Arquitetura baseada em componentes React
- **File-based Routing** - Roteamento baseado em arquivos com React Router
- **Server State Management** - Gerenciamento de estado servidor com React Query
- **Variant-based Components** - Componentes com variantes usando CVA
- **Composition Pattern** - Padrão de composição com Radix Slot
- **Path Aliasing** - Alias de caminhos (`@/` aponta para `src/`)

<BR>

## ⚙️ Configuração do Projeto

### Pré-requisitos

- Node.js
- npm ou yarn

### Instalação

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd <nome-do-repositorio>
cd web
```

### 2. Instale as dependências:

```bash
npm install
```

### 3. Execute o servidor de desenvolvimento:

```bash
npm run dev
```

### 4. Acesse a aplicação em `http://localhost:5173`

<br>

### Scripts Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Gera build de produção
- `npm run preview` - Preview do build de produção

### Backend

Lembre-se que o projeto consome uma API e esta deve estar rodando na porta 3333. Certifique-se de que o backend esteja configurado e executando antes de iniciar o frontend.
