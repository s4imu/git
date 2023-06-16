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