# 🚀 Project Root - Backend API (Core Engine)

### 📝 Descrição
Esta é a engine central da **Loja Drip**, uma API RESTful robusta construída com **Node.js**. O sistema gerencia toda a inteligência de negócio, desde a autenticação de usuários até o controle complexo de estoque e produtos. 

A arquitetura foi desenhada seguindo o padrão de **Camadas (Controller-Service-Model)**, garantindo que o código seja fácil de testar, escalar e manter. Utilizamos o **Sequelize** para mediar a comunicação com o banco de dados **PostgreSQL (Supabase)**, garantindo integridade e performance.

---

### 🛠️ Tecnologias de Elite
* **Runtime:** Node.js (v18+)
* **Framework:** Express.js
* **Persistência:** PostgreSQL & Sequelize ORM
* **Segurança:** JWT (JSON Web Tokens) & Bcrypt (Hash de alta segurança)
* **Documentação:** Swagger UI
* **Banco de Dados Cloud:** Supabase

---

### ⚙️ Configuração do Ambiente

1. **Clone este repositório:**
   ```bash
   git clone <link-do-seu-repo>
   cd project-root
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Variáveis de Ambiente (.env):**
   Crie um arquivo `.env` na raiz e configure suas credenciais (não esqueça de usar o **Connection Pooling** do Supabase para evitar erros de rede):
   ```env
   PORT=3001
   DB_HOST=aws-1-sa-east-1.pooler.supabase.com
   DB_USER=postgres.wmmkpnjysiacypqojklz
   DB_PASS=sua_senha_secreta
   DB_NAME=postgres
   DB_PORT=6543
   JWT_SECRET=sua_chave_jwt_gerada
   ```

---

### 🚀 Executando a Aplicação

* **Modo Desenvolvimento (com auto-reload):**
    ```bash
    npm run dev
    ```
* **Modo Produção:**
    ```bash
    npm start
    ```
> A API estará disponível em: `http://localhost:3001`

---

### 📂 Arquitetura do Sistema
```text
src/
├── server.js        # Ponto de entrada e inicialização
├── app.js           # Middlewares e configurações Express
├── config/          # Ajustes de DB e variáveis globais
├── controllers/     # Orquestração das requisições (Entrada/Saída)
├── services/        # O "Coração": Onde a lógica de negócio acontece
├── models/          # Definição das tabelas e esquemas (Sequelize)
├── routes/          # Mapa de caminhos da API
└── middlewares/     # Guardiões de segurança (Auth JWT)
```

---

### 🔑 Funcionalidades Principais
* **Gestão de Identidade:** Cadastro e login com senhas criptografadas.
* **Segurança de Rotas:** Bloqueio de áreas administrativas via Token JWT.
* **Catálogo Dinâmico:** CRUD completo de produtos, categorias e variações.
* **Upload de Assets:** Suporte para integração de imagens de produtos.
* **Sincronização Automática:** Auto-criação de tabelas via Sequelize Sync.

---

### 📖 Documentação Interativa
Navegue pelos endpoints e teste a API em tempo real:
`http://localhost:3001/api-docs`

---

### 🤝 Como Contribuir
1. Faça um **Fork** do projeto.
2. Crie sua Branch: `git checkout -b feature/nova-funcionalidade`.
3. Commit suas mudanças: `git commit -m 'feat: add nova funcionalidade'`.
4. Push para a Branch: `git push origin feature/nova-funcionalidade`.
5. Abra um **Pull Request**.

---

### 📜 Licença
Distribuído sob a licença **ISC**.
