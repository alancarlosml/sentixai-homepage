# SentixAI Backend - Contact API

Este é o back-end em FastAPI para armazenar contatos recebidos através do formulário do site. Ele utiliza PostgreSQL como banco de dados e está configurado para ser executado via Docker Compose.

## Estrutura do Projeto

- `backend/`: Código fonte da API FastAPI.
- `docker-compose.yml`: Configuração do Docker para subir a API e o Banco de Dados.
- `.env`: Variáveis de ambiente (credenciais do banco).

## Como subir na VPS

### Pré-requisitos
- Docker instalado na VPS.
- Docker Compose instalado na VPS.

### Passo a Passo

1. **Clone ou suba os arquivos para sua VPS**:
   Você pode usar Git ou SCP para mover a pasta do projeto para o servidor.

2. **Configure as credenciais**:
   Edite o arquivo `.env` para alterar as senhas padrões (opcional, mas recomendado).

3. **Suba os containers**:
   No terminal da sua VPS, dentro da pasta raiz do projeto, execute:
   ```bash
   docker-compose up -d --build
   ```

4. **Acesse a API**:
   - A API estará rodando na porta `8000`.
   - Documentação interativa (Swagger): `http://seu-ip-vps:8000/docs`

## Notas Importantes
- O formulário no `index.html` já está configurado para enviar os dados para `http://localhost:8000/contacts/`. **Lembre-se de alterar este URL no index.html para o IP público da sua VPS ou seu domínio antes de subir o site.**
- O banco de dados persiste os dados em um volume chamado `postgres_data`.
