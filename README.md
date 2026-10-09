# Desenvolvimento Web II — N1

Projeto desenvolvido para a atividade avaliativa N1 da disciplina de **Programação Web II**, utilizando Java com Spring Boot no backend e React com TypeScript no frontend.

O sistema permite realizar operações de cadastro, consulta, edição e exclusão de usuários, permissões e produtos, seguindo a arquitetura em camadas trabalhada durante as aulas.

## Tecnologias utilizadas

**Backend**
- Java 21
- Spring Boot 4.1.0
- Maven
- Spring Data JPA
- Spring Web
- Spring Security
- H2 Database

**Frontend**
- React
- TypeScript
- Vite
- Axios

## Funcionalidades

O sistema possui três módulos principais:

**Usuários**
- Cadastrar usuários
- Listar usuários cadastrados
- Editar informações
- Excluir usuários

**Permissões**
- Cadastrar permissões
- Listar permissões
- Editar permissões
- Excluir permissões

**Produtos**
- Cadastrar produtos
- Listar produtos
- Editar produtos
- Excluir produtos
- Validar o preço, impedindo valores negativos

## Estrutura do projeto

O backend está organizado em quatro camadas:

- `model`: entidades do sistema.
- `repository`: acesso ao banco de dados.
- `service`: regras de negócio.
- `controller`: endpoints da API REST.

O frontend está localizado em `src/main/frontend` e contém os componentes, formulários e páginas responsáveis pela interação com o usuário.

## Como executar

### Pré-requisitos

Para executar o projeto, é necessário ter instalado:

- JDK 21
- Maven 3.9 ou superior
- Node.js 22.12 ou superior (ou versão 24)
- npm

### 1. Clonar o repositório

```bash
git clone https://github.com/Z3NYN/desenvolvimento-web2.git
cd desenvolvimento-web2
```

### 2. Executar o backend

Na raiz do projeto:

```bash
mvn clean verify
mvn spring-boot:run
```

O backend será iniciado em:

`http://localhost:8080`

### 3. Executar o frontend

Em outro terminal, a partir da raiz do projeto:

```bash
cd src/main/frontend
npm ci
npm run dev
```

Acesse no navegador:

`http://localhost:5173`

## Banco de dados

O projeto utiliza o banco de dados H2, configurado para armazenar os dados localmente em arquivo.

Por isso, não é necessário instalar ou configurar um servidor de banco de dados externo para executar a aplicação.

## Endpoints da API

| Recurso | Endpoint |
|---|---|
| Usuários | `/api/usuarios` |
| Permissões | `/api/permissoes` |
| Produtos | `/api/produtos` |

Os recursos utilizam os seguintes métodos HTTP:

| Método | Operação |
|---|---|
| GET | Consultar ou listar registros |
| POST | Cadastrar um registro |
| PUT | Atualizar um registro |
| DELETE | Excluir um registro |

## Observações

- A aplicação utiliza uma API REST para comunicação entre frontend e backend.
- As operações realizadas no frontend atualizam as listagens de registros.
- As validações de regras de negócio são realizadas na camada de serviço.
- A senha dos usuários não é exibida nas respostas da API.
- O projeto foi desenvolvido para fins acadêmicos, sem implementação de autenticação de usuários.

## Atividade

**Disciplina:** Programação Web II  
**Avaliação:** N1  
**Repositório:** https://github.com/Z3NYN/desenvolvimento-web2
