# PirataFlix 🎬
Uma aplicação web completa para catalogar e gerenciar uma coleção de filmes, com funcionalidades distintas para usuários e administradores.

PirataFlix é um projeto Full Stack que permite aos usuários navegar por um catálogo de filmes, criar uma lista de interesse pessoal (watchlist), marcar filmes como assistidos e, para administradores, gerenciar todo o acervo de filmes através de operações de CRUD (Criar, Ler, Atualizar, Deletar).

<div style="display: flex; gap: 10px; flex-wrap: wrap;"> 
  <img align="center" alt="Javascript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/> 
  <img align="center" alt="React" src="https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB&style=for-the-badge"/> 
  <img align="center" alt="Node.js" src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white"/> 
  <img align="center" alt="Express" src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white"/> 
  <img align="center" alt="Bootstrap" src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white"/> 
  <img align="center" alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/> 
  <img align="center" alt="RavenDB" src="https://img.shields.io/badge/RavenDB-CC0000?style=for-the-badge&logo=raven&logoColor=white"/> 
  <img align="center" alt="Git" src="https://img.shields.io/badge/Git-F05033?style=for-the-badge&logo=git&logoColor=white"/> 
  <img align="center" alt="GitHub" src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/> 
</div>

---

## 🚀 Funcionalidades Implementadas
Autenticação de Usuários: Sistema completo de cadastro e login.  
A sessão do usuário é persistida no localStorage.

### Dois Papéis de Acesso:
#### Usuário (user):

- Navega pelo catálogo completo de filmes.
- Adiciona e remove filmes de sua "Lista de Interesse".
- Move filmes da "Lista de Interesse" para a lista de "Assistidos".
- Visualiza seu perfil com nome, email e a lista de filmes já assistidos.

#### Administrador (admin):
- Possui uma tela de administração (/tela-adm) dedicada.
- Tem permissão total para Adicionar, Editar e Excluir qualquer filme do catálogo.

#### Interface Dinâmica:
- O layout se adapta com base no login e no papel do usuário.
- A Home page exibe a lista de interesse do usuário em um carrossel horizontal.
- Carrossel de destaques na página inicial.
--- 

## 🛠  Tecnologias Utilizadas
O projeto é construído com uma stack moderna de JavaScript, dividido em Backend e Frontend.

#### Backend (Servidor)
- Node.js: Ambiente de execução para o JavaScript no servidor.
- Express.js: Framework para a construção da API RESTful.
- RavenDB: Banco de dados NoSQL utilizado para persistir os dados de filmes e usuários.
- Bcrypt.js: Biblioteca para criptografia e verificação de senhas, garantindo a segurança das credenciais.
- CORS: Middleware para permitir requisições entre o frontend e o backend.

#### Frontend (Cliente)
- React.js: Biblioteca para a construção de interfaces de usuário reativas e componentizadas.
- React Router: Biblioteca para o gerenciamento de rotas e navegação na aplicação (Single Page Application).
- React Bootstrap: Framework de componentes de UI para um design responsivo e moderno.
- Fetch API: Utilizada para a comunicação e consumo da API RESTful do backend.

--- 

### ⚙️ Como rodar o projeto

```
# 1. Clonar o repositório
git clone https://github.com/seu-usuario/projeto-filmes.git
cd projeto-filmes

# 2. Instalar dependências
npm install

# 3. Rodar o frontend
npm start

# 4. Rodar o backend (certifique-se que está em http://localhost:5000)
npm run server
```
### Banco de Dados
Este projeto utiliza **RavenDB** (pode ser trocado por PostgreSQL).
- Instale e rode o RavenDB localmente na porta padrão (http://localhost:8080)
- Crie um banco de dados chamado filmesdb
- Configure a conexão no backend  
(.env): RAVEN_URL=http://localhost:8080  
RAVEN_DB=filmesdb

---

## 📡 Rotas principais (backend) 

### 👤 Usuários
POST /users/register → cadastro de usuário <br> 
 POST /users/login → login de usuário 

### 📡 Administrador
POST /movies → cria novo filme
PUT /movies/:id → atualiza filme existente
DELETE /movies/:id → remove filme

### 🎞 Filmes 
GET /movies → busca todos os filmes do catálogo 

### ⭐ Lista de Interesse 
GET /users/:id/listaInteresse → retorna lista de interesse do usuário <br> 
POST /users/:id/listaInteresse → adiciona filme à lista de interesse <br>
DELETE /users/:id/listaInteresse/:movieId → remove filme da lista de interesse 

### ✅ Lista de Assistidos
POST /users/:id/listaAssistido → move filme para lista de assistidos 


---
## 📸 Prints do sistema 

###  Lista de Interesse 
![Lista de Interesse](./Prints/lista.jpg) 

### Catálogo de Filmes 
![Catálogo de Filmes](./Prints/home.jpg) 

###  Filmes Assistidos
![Filmes Assistidos](./Prints/listaA.jpg)

### Tela do ADM
![Filmes Assistidos](./Prints/adm.jpg)
