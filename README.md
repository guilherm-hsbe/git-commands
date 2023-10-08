# Git Commands :octocat: 	
> Lista de comandos úteis para a utilização do **git**.

O Git é um sistema de controle de versão distribuído amplamente utilizado para rastrear e gerenciar alterações em projetos de software. Ele foi desenvolvido por Linus Torvalds em 2005 e é uma ferramenta essencial para colaboração e desenvolvimento de código-fonte. Aqui estão alguns pontos-chave sobre o Git:

1. **Controle de Versão**: O Git permite que os desenvolvedores acompanhem e registrem as alterações feitas em seus arquivos de código-fonte ao longo do tempo. Isso facilita a recuperação de versões anteriores, o rastreamento de quem fez quais alterações e a colaboração em equipe.

2. **Distribuído**: O Git é um sistema de controle de versão distribuído, o que significa que cada desenvolvedor tem uma cópia completa do repositório do projeto em sua máquina local. Isso permite que o trabalho seja feito offline e facilita a colaboração em equipe.

3. **Ramificação (Branching) e Mesclagem (Merging)**: Os desenvolvedores podem criar ramificações independentes do código principal para trabalhar em novos recursos ou correções de bugs sem afetar o código principal. Posteriormente, essas ramificações podem ser mescladas de volta ao ramo principal.

4. **Repositórios** Remotos: O Git suporta repositórios remotos, como o GitHub, GitLab e Bitbucket, que permitem que várias pessoas colaborem em um projeto de software de forma síncrona e assíncrona.

5. **Histórico de Commits**: Cada alteração no código é registrada como um "commit" no Git, e esses commits formam um histórico completo das alterações ao longo do tempo. Cada commit é acompanhado por uma mensagem que descreve a alteração.

6. **Integração com Ferramentas de Desenvolvimento**: O Git é amplamente suportado por várias ferramentas de desenvolvimento, IDEs (Ambientes de Desenvolvimento Integrado) e serviços de hospedagem de código, tornando-o uma escolha popular para desenvolvedores de software.

<hr>

### Obtendo e Criando Projetos

| Comando | Descrição |
| ------- | ----------- |
| `git init` | Inicializa um repo Git local |
| `git clone ssh://git@github.com/[nome_usuario]/[nome-repositorio].git` | Cria uma cópia de um repo remoto |
| `git clone https://github.com/nome_usuario/nome_repositorio.git` | Também cria uma cópia de um repo remoto, porém sem SSH |
| `git clone https://github.com/nome_usuario/nome_repositorio.git nome_diretorio_personalizado` | Clonar um repo remóto para um destino customizado |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
