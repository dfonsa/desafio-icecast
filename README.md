<<<<<<< HEAD
# Desafio Icecast com Docker

Este projeto configura um servidor Icecast e um proxy reverso Nginx usando Docker. O objetivo é criar um ambiente de streaming de áudio acessível através de um navegador web

## Estrutura do Projeto

- `Dockerfile` (Icecast): Configura a imagem Docker para o servidor Icecast
- `Dockerfile` (Nginx): Configura a imagem Docker para o Nginx como proxy reverso
- `docker-compose.yml`: Arquivo para definir e rodar os containers Docker
- `icecast.xml`: Configuração do servidor Icecast
- `nginx.conf`: Configuração do Nginx

## Passo a Passo

### 1. **Preparar o Ambiente**

Certifique-se de que o Docker e o Docker Compose estão instalados e funcionando

### 2. **Construir e Rodar os Containers**

No diretório do projeto, execute o seguinte comando para construir e iniciar os containers:

```bash
docker-compose build
docker-compose up -d

=======
# desafio-icecast
Desafio DevOps: Instalação e Configuração de Icecast com Docker e Nginx
>>>>>>> 4ebebffbe2d1611301cd3ca7638445c517554106
