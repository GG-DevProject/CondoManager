# CondoManager

**CondoManager** é um sistema de gerenciamento de condomínios desenvolvido para síndicos e administradores. Ele permite o controle de moradores, unidades, reservas, finanças, e manutenção. O projeto utiliza um stack moderno com Vue.js no frontend, Python no backend e MySQL com phpMyAdmin para o banco de dados. O backup dos dados é armazenado em formato JSON.

## Tecnologias Utilizadas

- **Frontend**: Vue.js, Vuetify (para uma interface dinâmica e responsiva)
- **Backend**: Flask (Python)
- **Banco de Dados**: MySQL (via phpMyAdmin)
- **Backup**: Arquivo JSON para armazenamento de backup

## Estrutura do Projeto

```
CondoManager/
├── backend/                      # Backend (Python)
│   ├── app.py                    # Arquivo principal do backend
│   ├── database.py               # Configurações do banco de dados
│   ├── models.py                 # Modelos do banco de dados
│   ├── routes.py                 # Rotas do sistema
│   ├── backup.json               # Backup do banco de dados
├── frontend/                     # Frontend (Vue.js)
│   ├── public/                   # Arquivos estáticos (HTML)
│   │   ├── index.html            # Página inicial
│   ├── src/                      # Código Vue.js
│   │   ├── components/           # Componentes Vue.js
│   │   │   ├── Dashboard.vue
│   │   │   ├── Financeiro.vue
│   │   │   ├── Manutencao.vue
│   │   │   ├── Reservas.vue
│   │   ├── App.vue               # Componente principal
│   │   ├── router.js             # Rotas do frontend
│   ├── vuetify.js                # Configuração do Vuetify
├── docker-compose.yml            # Configuração Docker
├── README.md                     # Documentação do projeto
```

## Funcionalidades

- **Cadastro de Moradores**: Cadastro, visualização e atualização de moradores.
- **Gestão de Unidades**: Controle de informações das unidades habitacionais.
- **Financeiro**: Controle de receitas e despesas do condomínio.
- **Reserva de Áreas Comuns**: Gestão de reservas de espaços comuns do condomínio.
- **Backup**: Armazenamento dos dados em formato JSON para restauração fácil.

## Requisitos

- **Python 3.x**
- **Vue.js 3.x**
- **MySQL**
- **phpMyAdmin**
- **Docker** (para facilitar o setup do ambiente)

## Como Executar

### 1. Backend (Python + Flask)

1. Navegue até a pasta `backend` e crie um ambiente virtual:
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Inicie o servidor backend:
   ```bash
   python app.py
   ```

### 2. Frontend (Vue.js + Vuetify)

1. Navegue até a pasta `frontend`:
   ```bash
   cd frontend
   ```

2. Instale as dependências do Vue.js:
   ```bash
   npm install
   ```

3. Inicie o servidor frontend:
   ```bash
   npm run serve
   ```

### 3. Banco de Dados (MySQL + phpMyAdmin)

1. Certifique-se de que você possui **Docker** instalado.
2. Execute o seguinte comando para iniciar os containers do banco de dados e phpMyAdmin:
   ```bash
   docker-compose up
   ```

### 4. Acessando o Sistema

- **Frontend**: Abra [http://localhost:8081](http://localhost:8081) para acessar a interface web.
- **Backend**: O servidor backend estará rodando em [http://localhost:5000](http://localhost:5000).
- **phpMyAdmin**: Acesse [http://localhost:8080](http://localhost:8080) para gerenciar o banco de dados.

## Rotas da API (Backend)

- **GET /moradores**: Retorna a lista de moradores.
- **GET /financeiro**: Retorna a lista de receitas e despesas.
- **GET /backup**: Gera um arquivo JSON com o backup completo dos dados.

## Como Fazer Backup

Você pode fazer backup manualmente dos dados do sistema ao acessar a rota:
```
GET /backup
```
Isso irá gerar um arquivo `backup.json` com todas as informações dos moradores, unidades, receitas e despesas.

## Contribuição

Se você quiser contribuir para o projeto, siga os passos:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nome-da-feature`).
3. Commit suas alterações (`git commit -m 'Adicionando nova feature'`).
4. Faça um push para sua branch (`git push origin feature/nome-da-feature`).
5. Abra um Pull Request.

---

**CondoManager** é uma plataforma flexível e fácil de usar para síndicos, com suporte para controle de moradores, finanças e reservas, além de backup fácil em JSON para garantir a segurança dos dados.

--- 
