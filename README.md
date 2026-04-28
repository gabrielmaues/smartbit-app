Smartbit - Sistema de Gestão para Academias

O Smartbit é uma aplicação fictícia voltada para a gestão de academias, composta por:

Uma interface web que permite o pré-cadastro de clientes e oferece uma área autenticada para gerenciamento de matrículas
Um aplicativo mobile onde os usuários podem realizar login e registrar suas medidas corporais

Este projeto não foi desenvolvido por mim. Ele foi utilizado como base durante o curso "Universo Robot Framework", com o objetivo de implementar um projeto de automação de testes utilizando Robot Framework.

---

## Como subir a aplicação

### Pré-requisitos

- Node.js
- Docker Desktop

### Clonar o repositório

```
git clone https://github.com/gabrielmaues/smartbit-app.git
cd smartbit
```

### Instalar dependências

```
cd api
npm install

cd ..
cd web
npm install
```

### Subir container do banco de dados Postgres

Na raiz do projeto:
```
docker compose up -d
```

Com base nos dados do `docker-compose.yml`:
- Acessar o **pgadmin** em `http://localhost:15432` e fazer login
- Criar/configurar banco de dados `smartbit`

Inicializar estrutura do banco de dados:
```
cd api
./setup.sh
```

### Subir API e servidor web

```
cd api
npm run dev

cd ..
cd web
npm run dev
```

Acessar `http://localhost:3000` para testar a aplicação.
