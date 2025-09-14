# 🎬 Catálogo de Filmes 
Aplicação web feita em **React** com integração a um backend em **Node.js/Express**. 
O sistema permite que usuários façam login/cadastro, adicionem filmes à lista de interesse, marquem como assistidos e naveguem pelo catálogo completo de filmes. 
E o administrador pode fazer CRUD completo de filmes (criar, listar, atualizar, excluir).

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

### 🚀 Funcionalidades
- Cadastro e login de usuários
- Adicionar/remover filmes da lista de interesse 
- Marcar filmes como assistidos - Visualizar catálogo de filmes
- Interface responsiva com **React Bootstrap**

### 👩‍💼 Administrador 
- CRUD completo de filmes (criar, listar, atualizar, excluir)
- Gerenciar usuários 
  
--- 

### 🛠 Tecnologias Utilizadas 
- **Frontend:** React, React Router DOM, React Bootstrap 
- **Backend:** Node.js / Express 
-**Banco de Dados:** RavenDB noSQL ou PostgreSQL 
- **Outros:** Fetch API para comunicação entre front e back

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
