# Git Commands

### Obtendo e Criando Projetos

| Comando | Descrição |
| ------- | ----------- |
| `git init` | Inicializa um repo Git local |
| `git clone ssh://git@github.com/[nome_usuario]/[nome-repositorio].git` | Cria uma cópia de um repo remoto |
| `git clone https://github.com/nome_usuario/nome_repositorio.git` | Também cria uma cópia de um repo remoto, porém sem SSH |
| `git clone https://github.com/nome_usuario/nome_repositorio.git nome_diretorio_personalizado` | Clonar um repo remóto para um destino customizado |

### Snapshot

| Comando | Descrição |
| ------- | ----------- |
| `git status` | Verificar status |
| `git add [nome-do-arquivo.txt]` | Adicionar um arquivo à área de preparação (staging) |
| `git add -A` | Adicionar todos os arquivos novos e modificados à área de preparação (staging) |
| `git commit -m "[mensagem de commit]"` | Confirmar as alterações |
| `git rm -r [nome-do-arquivo.txt]` | Remover um arquivo (ou pasta) |

### Staging (Patch Interativo: `add -p`)
| Comando | Descrição |
| ------- | ----------- |
| **y** (yes) | Adicione esta parte à área de stage |
| **n** (no) | Não adicione esta parte à área de stage |
| **a** (all) | Adicione esta parte e todos os pedaços restantes no arquivo à área de stage |
| **d** (diff) | Não adicione esta parte nem nenhum dos pedaços restantes no arquivo à área de stage |
| **g** (select) | Selecione um pedaço para acessar |
| **/** (search) | Pesquise um pedaço que corresponda à expressão regular fornecida |
| **j** (undefined-next) | Deixe este pedaço indefinido e vá para o próximo pedaço indefinido |
| **J** (undefined-next-undef) | Deixe este pedaço indefinido e vá para o próximo pedaço |
| **k** (undefined-before) | Deixe este pedaço indefinido e vá para o pedaço indefinido anterior |
| **K** (undefined-before-undef) | Deixe este pedaço indefinido e vá para o pedaço anterior |
| **s** (split) | Divida o pedaço atual em pedaços menores |
| **e** (edit) | Edite manualmente o pedaço atual |
| **?** (help) | Exibe ajuda com informações sobre as opções disponíveis |

### Ramificação e Fusão

| Comando | Descrição |
| ------- | ----------- |
| `git branch` | Listar ramificações (o asterisco denota a ramificação atual) |
| `git branch -a` | Listar todas as ramificações (locais e remotas) |
| `git branch [nome da ramificação]` | Criar uma nova ramificação |
| `git branch -d [nome da ramificação]` | Excluir uma ramificação |
| `git push origin --delete [nome da ramificação]` | Excluir uma ramificação remota |
| `git checkout -b [nome da ramificação]` | Criar uma nova ramificação e alternar para ela |
| `git checkout -b [nome da ramificação] origin/[nome da ramificação]` | Clonar uma ramificação remota e alternar para ela |
| `git branch -m [nome da ramificação antiga] [nome da ramificação nova]` | Renomear uma ramificação local |
| `git checkout [nome da ramificação]` | Alternar para uma ramificação |
| `git checkout -` | Alternar para a última ramificação verificada |
| `git checkout -- [nome-do-arquivo.txt]` | Descartar alterações em um arquivo |
| `git merge [nome da ramificação]` | Fundir uma ramificação na ramificação ativa |
| `git merge [ramificação de origem] [ramificação de destino]` | Fundir uma ramificação em uma ramificação de destino |
| `git stash` | Armazenar alterações em um diretório de trabalho sujo |
| `git stash clear` | Remover todas as entradas armazenadas |

### Compartilhando e Atualizando Projetos

| Comando | Descrição |
| ------- | ----------- |
| `git push` | Enviar alterações para o repositório remoto (ramificação lembrada) |
| `git push origin [nome da ramificação]` | Enviar uma ramificação para o seu repositório remoto |
| `git push -u origin [nome da ramificação]` | Enviar alterações para o repositório remoto (e lembrar da ramificação) |
| `git push origin --delete [nome da ramificação]` | Excluir uma ramificação remota |
| `git push --force` | Forçar a atualização do repositório remoto (tenha cuidado com esse comando) |
| `git pull` | Atualizar o repositório local para o commit mais recente |
| `git pull origin [nome da ramificação]` | Puxar alterações do repositório remoto |
| `git remote add origin ssh://git@github.com/[nome-de-usuário]/[nome-do-repositório].git` | Adicionar um repositório remoto |
| `git remote set-url origin ssh://git@github.com/[nome-de-usuário]/[nome-do-repositório].git` | Definir a ramificação de origem de um repositório para SSH |
| `git fetch` | Buscar as atualizações do repositório remoto |
| `git pull --rebase` | Atualizar o repositório local com rebase |
| `git push --tags` | Enviar todas as tags para o repositório remoto |
| `git push origin --all` | Enviar todas as ramificações locais para o repositório remoto |
| `git remote -v` | Listar URLs dos repositórios remotos |
| `git remote remove origin` | Remover um repositório remoto associado |

### Inspeção e Comparação

| Comando | Descrição |
| ------- | ----------- |
| `git log` | Ver alterações |
| `git log --summary` | Ver alterações (detalhadas) |
| `git log --oneline` | Ver alterações (breve) |
| `git diff` | Visualizar alterações em todos os arquivos |
| `git diff [ramificação de origem] [ramificação de destino]` | Visualizar alterações antes da fusão |
| `git diff [nome-do-arquivo]` | Visualizar alterações não confirmadas em uma arquivo |
| `git diff [commit-anterior] [commit-atual] -- [nome-do-arquivo]` | Comparar alterações em commits específicos |
| `git tag` | Adicionar e gerenciar tags de commits |
| `git reflog` | Exibir o registro de referências e recuperar commits perdidos |
| `git cherry-pick` | Aplicar commits específicos de uma ramificação para outra |
| `git rebase` | Reorganizar o histórico de commits ou integrar commits de forma flexível |
| `git blame [nome-do-arquivo]` | Rastrear a autoria de cada linha em um arquivo |
| `git log --grep [termo]` | Procurar commits que contenham um termo específico no log de commit |
| `git log -- [caminho-do-arquivo]` | Ver o histórico de commits específico de um arquivo |
| `git log --stat` | Exibir estatísticas resumidas de cada commit |
| `git log --abbrev-commit` | Exibir hashes de commit abreviados |

### Navegação e Histórico no Terminal

| Comando               | Descrição                                    |
| --------------------- | -------------------------------------------- |
| `history`             | Lista os comandos usados recentemente        |
| `!n`                  | Executa o comando de número `n` no histórico |
| `!!`                  | Executa o último comando novamente           |
| `Ctrl + r`            | Busca interativa no histórico de comandos    |
| `clear` ou `Ctrl + l` | Limpa a tela do terminal                     |
| `cd -`                | Vai para o diretório anterior                |

### Git Log

| Comando                                      | Descrição                                                          |
| -------------------------------------------- | ------------------------------------------------------------------ |
| `git log --oneline --graph --decorate --all` | Visualização compacta e completa do histórico com gráfico          |
| `git show [hash]`                            | Exibe detalhes de um commit específico                             |
| `git log -p`                                 | Exibe o diff (mudanças de código) junto com cada commit            |
| `git log --author="nome"`                    | Filtra commits por autor                                           |
| `git log --since="1 week ago"`               | Mostra commits a partir de uma data                                |
| `git log --until="2024-12-31"`               | Mostra commits até uma data.                                       |
| `git log --grep="palavra"`                   | Filtra por palavra-chave na mensagem do commit.                    |
| `git log <arquivo>`                          | Mostra o histórico de commits que alteraram um arquivo específico. |

### Gerenciando Credenciais :label:

| Comando | Descrição |
| ------- | ----------- |
| `git config --list` | Lista todas as configurações do Git em seu sistema |
| `git config user.name "Meu Nome"` | Configurar nome |
| `git config user.email "meu-email@example.com"` | Configurar email |
| `git config credential.username "seu-usuario"` | Definir credenciais de nome de usuário HTTPS |
| `git config credential.helper store` | Definir credenciais de senha HTTPS |
| `git config --global --unset user.name` | Remover credenciais de usuário globais |
| `git config --global --unset user.email` | Remover credenciais de email globais |
| `git config --unset user.name` | Remover credenciais de email locais |
| `git config --unset user.email` | Remover credenciais de usuário locais |
| `git credential reject` | Remover credenciais em cache |

### Chaves SSH :key:

#### Criando chaves SSH (processo padrão)
| Comando | Descrição |
| ------- | ----------- |
| `ssh-keygen -t ed25519 -C "email@exemplo.com"` | Gerar um novo par de chaves SSH |
| `ssh-keygen -t rsa -b 4096 -C "exemplo@exemplo.com"` | Gerar um novo par de chaves SSH (Nota: Use este você estiver usando um sistema legado que não suporta o **algoritmo Ed25519**) |]
| `eval "$(ssh-agent -s)"` | Inicializar o serviço do agente-ssh |
| `ssh-add ~/.ssh/chave-privada` | Adicionar a chave SSH ao agente-ssh |
| `clip < ~/.ssh/id_ed25519.pub` | Copiar o conteúdo da chave pública para então criar uma nova chave pública na interface do GitHub, e colar o conteúdo da chave (Nota: nem todo sistema possui a mesma nomenclatura de cópia de conteúdo de arquivo) |
| `ssh -T git@github.com` | Estalecer conexão da SSH com o GitHub |

#### Gerenciando chaves SSH
| Comando | Descrição |
| ------- | ----------- |
| `ssh -T git@github.com` | Verifica se sua chave SSH está configurada corretamente para se comunicar com o GitHub |
| `ssh-keygen -p -f ~/.ssh/chave-privada` | Trocar a frase de segurança de uma chave SSH privada |
| `ssh-keygen -f [caminho-da-chave]` | Gerar um par de chaves SSH com um nome específico |
| `ssh-copy-id [usuário@host]` | Copiar a chave pública para um servidor remoto |
| `ssh-add [caminho-da-chave-privada]` | Adicionar uma chave privada à autenticação SSH |
| `ssh-agent` | Iniciar o agente SSH para gerenciar chaves privadas |
| `ssh-agent -s` | Configurar o ambiente para usar o agente SSH |
| `ssh-add -l` | Listar todas as chaves privadas atualmente carregadas no agente SSH |
| `ssh-add -D` | Remover todas as chaves privadas carregadas no agente SSH |
| `ssh-keyscan [host] >> ~/.ssh/known_hosts` | Escanear e adicionar a chave pública de um servidor remoto aos hosts conhecidos |
| `ssh-keygen -R [host]` | Remover a chave pública de um servidor remoto dos hosts conhecidos |
| `chmod 600 ~/.ssh/id_rsa` | Configurar permissões restritas em uma chave privada |
| `chmod 644 ~/.ssh/id_rsa.pub` | Configurar permissões em uma chave pública |
| `ssh-keygen -p -f [caminho-da-chave]` | Alterar a senha de uma chave privada existente |
