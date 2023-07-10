# Comandos

**init:** inicializar um repositorio

 **status:** usado para verificar o estado atual do repositório Git, mostrando quais arquivos foram modificados, quais estão prontos para serem confirmados e quais não estão sendo rastreados pelo Git.

**add:** usado para adicionar alterações ou novos arquivos ao stage (área de preparação) do Git, permitindo que você selecione as alterações específicas que deseja incluir no próximo commit

**commit:** usado para criar um novo commit no repositório Git, salvando as alterações no histórico do projeto. É importante fornecer uma mensagem descritiva para o commit, para que outras pessoas possam entender facilmente as alterações realizadas.

~~~bash
git commit -m "Mensagem do commit"
~~~
 
**push:** usado para enviar os commits locais para um repositório remoto, atualizando o branch remoto correspondente com as alterações confirmadas. 

~~~bash
git push <nome_remoto> <nome_branch>
~~~

**pull:** usado para buscar as alterações mais recentes de um repositório remoto e mesclá-las automaticamente com o branch local atual. 

~~~bash
git pull <nome_remoto> <nome_branch>
~~~

<nome_remoto>: É o nome do repositório remoto para onde você deseja enviar os commits.

<nome_branch>: É o nome do branch (ramo) local que você deseja enviar para o repositório remoto. 

**fetch:** Usado para buscar as alterações mais recentes de um repositório remoto para o repositório local, atualizando as referências remotas locais sem mesclar automaticamente as alterações com o branch local atual. 

~~~bash
git fetch <nome_remoto> 
~~~

**merge:** usado para combinar as alterações de um branch com outro branch no repositório Git, criando um novo commit que incorpora as alterações dos dois branches

~~~bash
git merge <branch_de_origem>
~~~

<branch_de_origem>: É o nome do branch de onde você deseja mesclar as alterações. Por exemplo, pode ser o nome de um branch remoto ou local, como "feature/branch" ou "origin/branch".

**clone:** usado para criar uma cópia local de um repositório Git remoto. Ele baixa todo o histórico de commits, ramos (branches), tags e outros objetos do repositório remoto para o diretório de trabalho local.

**rm:**  usado para remover arquivos ou diretórios do repositório Git. Ele indica ao Git que você deseja que um determinado arquivo ou diretório seja removido do controle de versão

**log:** sado para exibir o histórico de commits de um repositório Git. Ele mostra informações detalhadas sobre os commits realizados, como o autor, a data, a mensagem de commit e o hash do commit.

**mv:** usado para renomear ou mover arquivos ou diretórios no repositório Git. Ele permite que você renomeie um arquivo ou mova-o para um diretório diferente no repositório Git, mantendo o controle de versão adequado do arquivo. Serve para renomear o arquivo também

~~~bash
git mv <arquivo_ou_diretório_atual> <novo_arquivo_ou_diretório>
~~~

**git checkout:** permite várias ações como:
* Alternar entre branches:
~~~bash
git checkout <nome_do_branch>
~~~

* Criar e alternar para uma nova branch:

~~~bash
git checkout -b <nome_do_branch>
~~~

*  verificar um commit específico em vez de um branch. No entanto, seu repositório entrará no chamado modo "detached HEAD", o que significa que você estará verificando um commit específico, mas não estará em um branch. Tenha cuidado ao fazer alterações nesse estado, pois elas podem ser perdidas:

~~~bash
git checkout <hash_do_commit>
~~~

* reverter as alterações não confirmadas de um arquivo específico para a versão mais recente no commit anterior.

~~~bash
git checkout -- <caminho_do_arquivo>
~~~

* descartar todas as alterações não confirmadas em todos os arquivos no diretório de trabalho, revertendo-os para as versões mais recentes registradas nos commits anteriores.

~~~bash
git checkout -- 
~~~

* sempre commit suas alterações antes de trocar de branches
* branches para desenvolvimento de novas criações devem ser cópias da Main

**reset:** usado para desfazer alterações em um repositório Git. Ele permite redefinir o estado do repositório para um commit anterior, descartando commits, desfazendo alterações e movendo o ponteiro HEAD e/ou ramos para um commit específico.

~~~bash
git reset --hard <commit>
git reset --hard <branch>
~~~

**branch:** usado para listar, criar e excluir branches (ramos) em um repositório Git.

* **git branch** - Listar branches
* **git branch <nome_do_novo_branch>:** - Criar novo branch
* **git branch -d <nome_do_branch>:** - Deletar branch


**stash:** usado para armazenar temporariamente as alterações não confirmadas, permitindo que você limpe seu diretório de trabalho e volte a um estado limpo antes de alternar para outra tarefa ou ramificação.

pode ser útil em várias situações, como quando você está no meio de um trabalho em progresso e precisa alternar para outra tarefa urgente ou ramificação. Ao invés de fazer um commit inacabado, você pode usar o "git stash" para guardar suas alterações em um local seguro e voltar a um estado limpo do repositório.

**stash list:** utilizado para visualizar a lista de stashes disponíveis no repositório. Ele mostra informações sobre cada stash, como o índice do stash, o ramo em que o stash foi criado e uma mensagem descritiva opcional fornecida ao criar o stash.


**stash apply:** utilizado para aplicar as alterações de um stash salvo de volta ao seu diretório de trabalho

~~~bash
    git stash apply stash@{n}
~~~

Onde "n" é o índice do stash que você deseja aplicar. Por exemplo, "stash@{0}" refere-se ao stash mais recente.

**stash clear:**  usado para limpar completamente a pilha de stashes, removendo todos os stashes armazenados no repositório.

**stash drop:** utilizado para remover um stash específico da pilha de stashes do repositório. 

~~~bash
    git stash drop stash@{n}
~~~

**tag:**  usado para criar, listar e gerenciar tags (marcas) em um repositório. As tags são usadas para marcar pontos específicos na história do seu projeto, geralmente para marcar versões ou lançamentos importantes.

~~~bash
    git tag -a nome_da_tag -m "Mensagem da tag"
~~~
 
 Você também pode:

 * Listar Tags:
 ~~~bash
    git tag
 ~~~

* Exibir infos detalhadas 

 * Listar Tags:
 ~~~bash
    git show nome_da_tag
 ~~~

 * Compartilhar tags: Por padrão, as tags não são enviadas automaticamente para um repositório remoto ao executar "git push". Para enviar tags específicas para um repositório remoto, use o comando:
 ~~~bash
    git push origin nome_da_tag
 ~~~

* Deletar tags: Para remover uma tag existente, use o seguinte comando:
 ~~~bash
    git tag -d nome_da_tag
 ~~~

**.gitignore:** arquivo utilizado pelo Git para especificar quais arquivos e diretórios devem ser ignorados durante o versionamento de um repositório.

* **arquivo.txt** - Ignorar um arquivo específico
* ***.log** - Ignorar todos os arquivos com uma determinada extensão
* **diretorio/** - Ignorar todos os arquivos em um diretório
* **diretorio/*** - Ignorar arquivos em um diretório específico, mas não em subdiretórios:
* ****/diretorio/** - Ignorar arquivos em todos os diretórios com um nome específico: