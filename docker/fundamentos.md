# Notas Teóricas - Docker

- **Docker Daemon**: Gerencia criação e execução de containers.
- **Registry**: Repositório de imagens.
- **Isolamento**: Utiliza Cgroups e Namespaces.
- **Vantagem**: Inicialização rápida sem carregar SO completo.

---
## 🛠️ Hands-on: Prática e Troubleshooting

### 1. Gestão de Imagens e Tags
- **Desafio de Versão:** Imagens como o Rocky Linux exigem tags específicas. A tentativa de rodar apenas `rockylinux` falha; o correto é utilizar `rockylinux:9`.
- **Otimização de Disco:** Identifiquei imagens de banco de dados (Mongo, MySQL, Postgres) ocupando mais de 3GB. Realizei a limpeza seletiva para manter apenas o essencial (Ubuntu e Hello-world).

### 2. Isolamento de Distribuições
- **Conceito Chave:** Mesmo utilizando **Rocky Linux** como host, é possível rodar containers **Ubuntu** com isolamento total de processos.
- **Gerenciadores de Pacote:** Dentro de um container, os comandos devem seguir a distribuição da imagem. 
  - No Ubuntu, utilizamos `apt`.
  - O comando `dnf` (nativo do Rocky) não existe dentro do container Ubuntu.

### 3. Comandos Úteis do Dia
```bash
# Entrar no container de forma interativa
docker container run -it ubuntu /bin/bash

# Atualizar repositórios e instalar pacotes (Essencial para imagens minimalistas)
apt update && apt install curl -y

# Validar instalação
curl --version


## ✅ Teste de Sincronização Remota
- Arquivo editado via terminal às 00:25.
