# 🎫 API de Ticket de Suporte

Esta API foi desenvolvida para gerenciar tickets de suporte técnico, permitindo aos usuários criar tickets solicitando suporte, atualizar as informações dos tickets, listar os tickets com possibilidade de filtro por status e atualizar o status de um ticket para "fechado".

## 🛠️ Tecnologias Utilizadas 

- 🟢 **Node.js**: Utilizado como runtime para executar o JavaScript no servidor, fornecendo a base para construir a API de suporte técnico com alto desempenho e eficiência.
- 🟡 **JavaScript**: Linguagem principal para desenvolvimento da lógica da API, manipulando requisições, respostas e implementando as funcionalidades de gerenciamento de tickets.

## ⚙️ Funcionalidades

- ✍️ **Criação de Tickets**: Criação de novos tickets com informações sobre o equipamento, problema e usuário.
- 🗒️ **Listagem de Tickets**: Exibe todos os tickets, com opção de filtrar por status (aberto ou fechado).
- 🔄 **Atualização de Tickets**: Atualiza informações de um ticket existente, como descrição e equipamento.
- ✅ **Fechamento de Tickets**: Altera o status do ticket para "fechado".
- ❌ **Exclusão de Tickets**: Exclui um ticket específico pelo ID.

## 🔗 Rotas 

### ✍️ Criar Ticket 

- **Método:** `POST`  
- **URL:** `/tickets`  
- **Descrição:** Cria um novo ticket de suporte.

**Dados:**
- `equipment` (string, obrigatório): Nome do equipamento (exemplo: computador)
- `description` (string, obrigatório): Descrição do problema.
- `user_name` (string, obrigatório): Nome do usuário que está criando o ticket.

---

### 📑 Obter Tickets 

- **Método:** `GET`  
- **URL:** `/tickets`  
- **Descrição:** Obtém uma lista de todos os tickets de suporte.

**Parâmetros de Consulta (Query Parameters):**
- `status` (string, opcional): Filtra os tickets pelo status ("open" ou "closed").

---

### 🔄 Atualizar Ticket 

- **Método:** `PUT`  
- **URL:** `/tickets/:id`  
- **Descrição:** Atualiza as informações de um ticket específico.

**Parâmetros de Rota:**
- `id` (UUID, obrigatório): ID do ticket.

**Parâmetros no Corpo (JSON):**
- `equipment` (string, obrigatório): Nome do equipamento (exemplo: computador)
- `description` (string, obrigatório): Descrição do problema.
- `user_name` (string, não altera)

---

### ✅ Fechar Ticket 

- **Método:** `PATCH`  
- **URL:** `/tickets/:id/status`  
- **Descrição:** Atualiza o status de um ticket para "fechado".

**Parâmetros de Rota:**
- `id` (UUID, obrigatório): ID do ticket.

---

### ❌ Excluir Ticket

- **Método:** `DELETE`  
- **URL:** `/tickets/:id`  
- **Descrição:** Exclui um ticket específico pelo seu ID.

**Parâmetros de Rota:**
- `id` (UUID, obrigatório): ID do ticket.

---

## 🚀 Como Executar o Projeto 

1. Clone este repositório:
```bash
git clone https://github.com/joschonarth/support-tickets.git
```

2. Navegue até a pasta do projeto:
```bash
cd support-tickets
```

3. Inicie o servidor:
```bash
npm run dev
```

🌐 O servidor estará rodando em `http://localhost:3333`.

## 🤝 Contribuições
Sinta-se à vontade para contribuir para este projeto. Para isso, faça um fork, crie sua feature branch e envie um pull request.