# Estudos de Containers de Sistema - LXD/LXC

Notas sobre o módulo de infraestrutura de containers utilizando LXD no **Rocky Linux**.

## Aprendizados Técnicos
- **LXD vs Docker**: Entendi que o LXD cria containers de sistema (como máquinas virtuais leves que compartilham o kernel do host), enquanto o Docker foca em containers de aplicação.
- **Uso de Recursos**: O container utiliza os recursos (CPU/RAM) do SO hospedeiro sob demanda, sem a sobrecarga de um Hypervisor.

## Desafios no Rocky Linux
- **Instalação**: Necessário utilizar o `snap` para instalar o LXD no Rocky Linux.
- **Storage Backend**: Devido a incompatibilidades de kernel com BTRFS/ZFS no ambiente atual, utilizei o backend `dir` durante o `lxd init`.
- **Permissões**: Configuração de grupos de usuário para permitir o comando `lxc` sem `sudo`.

## Comandos Utilizados
- Iniciar serviço: `sudo lxd init`
- Lançar container: `lxc launch ubuntu:22.04 meucontainer`
- Listar instâncias: `lxc list`
