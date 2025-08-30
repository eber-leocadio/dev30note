Boa! 💡 Vamos turbinar a **folha de cola em Markdown**.
Além dos comandos que já vimos, vou incluir os **básicos de login, autenticação e configuração**.

Aqui está a versão completa em **Markdown**:

---

# 🐳 Docker Cheat Sheet

## 🔑 Login & Configuração Básica

```bash
docker login                       # Faz login no Docker Hub
docker logout                      # Faz logout do Docker Hub
docker login <registry>            # Login em outro registry (ex: AWS ECR, GCP, Azure)
docker --config <caminho>          # Especifica diretório de configuração do Docker
docker info                        # Mostra informações da instalação
docker version                     # Mostra versão cliente/servidor do Docker
```

---

## 📦 Containers

```bash
docker ps                          # Lista containers em execução
docker ps -a                       # Lista todos os containers
docker run <imagem>                # Cria e inicia um container
docker run -d <imagem>             # Executa em background
docker run -it <imagem> sh         # Executa de forma interativa
docker start <container>           # Inicia container parado
docker stop <container>            # Para container em execução
docker restart <container>         # Reinicia container
docker rm <container>              # Remove container
docker logs <container>            # Mostra logs
docker exec -it <container> bash   # Acessa container em execução
```

---

## 📂 Imagens

```bash
docker images                      # Lista imagens locais
docker pull <imagem>               # Baixa imagem do Docker Hub
docker push <imagem>               # Envia imagem para o registry
docker rmi <imagem>                # Remove imagem
docker build -t <nome:tag> .       # Cria imagem a partir de um Dockerfile
docker tag <imagem> <repo:tag>     # Renomeia/tagueia imagem
```

---

## 💾 Volumes

```bash
docker volume ls                        # Lista volumes
docker volume create <nome>             # Cria volume
docker run -v <volume>:/caminho <img>   # Monta volume no container
docker volume inspect <volume>          # Inspeciona volume
docker volume rm <volume>               # Remove volume
```

---

## 🌐 Redes

```bash
docker network ls                          # Lista redes
docker network create <nome>               # Cria rede
docker network inspect <rede>              # Inspeciona rede
docker network connect <rede> <container>  # Conecta container à rede
docker network disconnect <rede> <cont>    # Desconecta container da rede
docker network rm <rede>                   # Remove rede
```

---

## ⚙️ Sistema

```bash
docker info             # Informações do Docker
docker stats            # Monitora containers em tempo real
docker system df        # Mostra uso de disco
docker system prune     # Limpa containers, imagens e volumes não usados
docker inspect <objeto> # Mostra detalhes (container, imagem, volume, rede)
```

---

## 🛠️ Docker Compose

```bash
docker compose up -d    # Sobe serviços
docker compose down     # Derruba serviços
docker compose ps       # Lista serviços em execução
docker compose logs     # Mostra logs
docker compose build    # Reconstrói imagens
docker compose restart  # Reinicia serviços
```

---

💡 **Dica Pro:**
Use `docker <comando> --help` para ver todas as opções disponíveis.

---

👉 Quer que eu monte esse **Markdown já com formatação em tabela** (colunas para "Comando" e "Descrição") para ficar ainda mais legível como referência rápida? 📑
