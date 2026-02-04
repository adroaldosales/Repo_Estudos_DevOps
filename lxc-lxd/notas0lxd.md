# 🚀 Containers de Sistema: LXC e LXD

Repositório de estudos focado no isolamento nativo do Kernel Linux (Namespaces e Cgroups).

## 🔹 Diferença Técnica
- **LXC**: É o motor de execução dos containers. Ele permite que o processo acredite que está em uma máquina isolada.
- **LXD**: É o "carro" que dirigimos. Ele fornece a interface de comando `lxc` para gerenciar as imagens e instâncias de forma simples.

## 🛠️ Desafios Superados no Rocky Linux
- **Instalação via Snap**: Necessário para garantir a versão mais estável do daemon.
- **Backend de Armazenamento**: Configurado como `dir` (diretório) devido às restrições de kernel para ZFS/BTRFS no ambiente.
- **Permissões**: Configuração do grupo `lxd` para acesso sem `sudo`.

## 📋 Comandos Práticos
- `lxc launch ubuntu:22.04 meucontainer` -> Cria e inicia o container.
- `lxc list` -> Exibe status e IP (ex: 10.144.209.103).
- `lxc exec meucontainer bash` -> Acesso ao shell interno.
- `lxc delete meucontainer --force` -> Remove a instância.
