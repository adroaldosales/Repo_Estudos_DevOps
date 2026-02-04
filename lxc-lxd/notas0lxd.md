# 🚀 Containers de Sistema: LXC e LXD

Repositório de estudos focado no isolamento nativo do Kernel Linux (Namespaces e Cgroups).

## 🔹 Diferença Técnica
- **LXC**: O motor de execução. Isola o processo para que ele pareça um SO independente.
- **LXD**: O gerenciador. Facilita o controle das instâncias via comando `lxc`.

## 🛠️ Setup no Rocky Linux
- **Storage**: Configurado como `dir` devido à compatibilidade do Kernel.
- **Primeiro Container**: `lxc launch ubuntu:22.04 meucontainer`.

## 📖 Guia de Boas Práticas (Git Commits)
Sempre utilizar o padrão **Conventional Commits** para um histórico profissional:
- `feat:` Novas funcionalidades ou pastas (ex: novo módulo).
- `fix:` Correção de erros em comandos ou scripts.
- `docs:` Alterações apenas em arquivos de texto/notas.
- `refactor:` Mudança na estrutura sem alterar a função (ex: renomear pastas).
- `chore:` Tarefas rotineiras ou manutenção.

*Nota: Sempre usar `-m` para evitar a abertura acidental do editor Vim.*
