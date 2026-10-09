# Desenvolvimento Web II

Projeto full stack desenvolvido durante a disciplina de **Programação Web II**, utilizando Spring Boot no backend e React com TypeScript no frontend.

O sistema permite gerenciar usuários, permissões e produtos por meio de operações de cadastro, consulta, edição e exclusão, utilizando uma API REST e uma arquitetura em camadas.

## Tecnologias utilizadas

### Backend
- Java 21
- Spring Boot 4.1.0
- Maven
- Spring Web
- Spring Data JPA
- Spring Security
- H2 Database
- PostgreSQL Driver

### Frontend
- React
- TypeScript
- Vite
- Axios

## Funcionalidades

O sistema possui operações de CRUD para três entidades:

**Usuários**
- Cadastro de usuários
- Listagem de usuários
- Edição de informações
- Exclusão de usuários

**Permissões**
- Cadastro de permissões
- Listagem de permissões
- Edição de permissões
- Exclusão de permissões

**Produtos**
- Cadastro de produtos
- Listagem de produtos
- Edição de produtos
- Exclusão de produtos
- Validação para impedir preços negativos

## Estrutura do projeto

O backend está organizado em camadas:

- `model` — Entidades do sistema.
- `repository` — Acesso e persistência dos dados.
- `service` — Regras de negócio.
- `controller` — Endpoints da API REST.

O frontend está localizado em `src/main/frontend`, com páginas e componentes responsáveis pela interface e comunicação com a API.

## Como executar

### Pré-requisitos

- JDK 21
- Maven 3.9 ou superior
- Node.js 22.12 ou superior, ou versão 24
- npm

### 1. Clonar o repositório

```bash
git clone https://github.com/Z3NYN/desenvolvimento-web2.git
cd desenvolvimento-web2
```

### 2. Iniciar o backend

Na raiz do projeto, execute:

```bash
mvn clean verify
mvn spring-boot:run
```

O backend estará disponível em `http://localhost:8080`.

### 3. Iniciar o frontend

Em outro terminal, a partir da raiz do projeto:

```bash
cd src/main/frontend
npm ci
npm run dev -- --port 5173 --strictPort
```

A aplicação estará disponível em `http://localhost:5173`.

## Banco de dados

O projeto utiliza H2 com persistência em arquivo local, permitindo manter os registros após reiniciar a aplicação.

Não é necessário instalar um servidor de banco de dados externo para executar o sistema.

## API REST

| Recurso | Endpoint |
|---|---|
| Usuários | `/api/usuarios` |
| Permissões | `/api/permissoes` |
| Produtos | `/api/produtos` |

Métodos HTTP disponíveis:

| Método | Descrição |
|---|---|
| GET | Listar ou consultar registros |
| POST | Cadastrar registros |
| PUT | Atualizar registros |
| DELETE | Excluir registros |

Para consultar um registro específico, atualizar ou excluir, utiliza-se o identificador na URL, como em `/api/produtos/{id}`.

## Observações

- A comunicação entre frontend e backend é realizada com Axios.
- As listagens são atualizadas após as operações de cadastro, edição e exclusão.
- As regras de negócio são implementadas na camada de serviço.
- A senha dos usuários não é retornada nas respostas da API.
- A autenticação de usuários ainda não foi implementada.

## Desenvolvimento

Projeto acadêmico desenvolvido como parte das atividades práticas da disciplina de Programação Web II.
