# Event Subscription System

## 📌 Sobre o Projeto
O **Event Subscription System** é uma API desenvolvida em **Spring Boot**, utilizando **MySQL** e **Docker**, que permite a gestão de inscrições em eventos. Os usuários podem se cadastrar em eventos, gerar links de indicação e visualizar rankings de indicações.

## 🚀 Tecnologias Utilizadas
- **Java 17**
- **Spring Boot** (Spring Framework, Spring Data JPA, Spring Web)
- **MySQL** (Banco de Dados Relacional)
- **Docker** (Para conteinerização)
- **Hibernate** (ORM para JPA)

## 🎯 Funcionalidades
1. **Inscrição**:
   - Os usuários podem se inscrever em eventos usando nome e e-mail.
2. **Geração de Link de Indicação**:
   - Um link único é gerado para cada inscrito, permitindo indicações.
3. **Ranking de Indicações**:
   - Um ranking exibe os usuários com mais indicações.
4. **Visualização de Indicações**:
   - Cada usuário pode ver quantas pessoas se inscreveram pelo seu link.

## 🏛 Arquitetura do Sistema
O sistema segue a arquitetura **MVC (Model-View-Controller)** e está estruturado da seguinte forma:

```
- br.com.nlw.events
    ├── controller   # Camada de Controllers (Endpoints da API)
    ├── service      # Camada de Serviços (Regras de negócio)
    ├── model        # Camada de Modelos (Entidades JPA)
    ├── repository   # Camada de Repositórios (Acesso ao Banco de Dados)
    ├── config       # Configurações e Integrações
```

## 🛠 Como Executar o Projeto
### 1️⃣ Clonar o repositório
```bash
git clone https://github.com/seu-usuario/event-subscription-system.git
cd event-subscription-system
```

### 2️⃣ Configurar o Banco de Dados (MySQL)
Certifique-se de ter o MySQL rodando e crie um banco de dados:
```sql
CREATE DATABASE event_db;
```

### 3️⃣ Configurar as Variáveis de Ambiente
Renomeie o arquivo **`.env.example`** para **`.env`** e configure os dados do banco de dados.

### 4️⃣ Executar o Projeto com Docker
```bash
docker-compose up --build
```

### 5️⃣ Acessar a API
A API estará disponível em: **http://localhost:8080**

## 📌 Endpoints da API
| Método | Rota                      | Descrição                      |
|---------|--------------------------|--------------------------------|
| GET     | `/events`                 | Lista todos os eventos        |
| POST    | `/events`                 | Cria um novo evento           |
| POST    | `/subscriptions`          | Realiza uma inscrição         |
| GET     | `/subscriptions/ranking`  | Retorna o ranking de indicações |

## 📜 Licença
Este projeto está licenciado sob a **MIT License** - veja o arquivo **LICENSE** para mais detalhes.

---
**Desenvolvido por [João Victor Asevedo](https://github.com/iamjvictor) 🚀**

