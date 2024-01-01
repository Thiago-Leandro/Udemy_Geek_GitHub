# Comandos Git apreendidos no curso da Geek University

## 1. Instalação do Git

Para instalar o Git, utilize o seguinte comando:

~~~
sudo apt-get install git
~~~

## 2. Verificar a Versão do Git

Para verificar a versão do Git instalada, utilize o seguinte comando:

~~~
git --version
~~~

## 3. Inicializar um Repositório Git

Para criar um novo repositório Git em um diretório existente, utilize o seguinte comando:

~~~
git init
~~~

## 4. Verificar o Status do Repositório

Para verificar o status do seu repositório, incluindo arquivos não rastreados e alterações no stage, utilize o seguinte comando:

~~~
git status
~~~

## 5. Configurar Informações de Usuário

Configure seu nome de usuário e endereço de email para seus commits:

~~~
git config user.name "Nome_Usuario"
git config user.email "Email_usuario"
~~~

Para configurações globais que se aplicam a todos os repositórios:

~~~
git config --global user.name "Nome_Usuario"
git config --global user.email "Email_usuario"
~~~

## 6. Adicionar Arquivos ao Stage

Adicione arquivos ao stage antes de realizar um commit:

~~~
git add .gitignore
git add programa1.html
git add programa2.html
git add .
~~~

## 7. Realizar um Commit

Para criar um commit com as alterações no stage, utilize o seguinte comando:

~~~
git commit -m "Meu primeiro commit"
~~~

## 8. Comandos Git para Logs

* Visualizar o Histórico de Commits
Para visualizar o histórico de commits do repositório:

~~~
git log
~~~

* Para visualizar o último commit:

~~~
git log -1
~~~

* Para visualizar o histórico de commits em uma única linha:

~~~
git log --oneline
~~~

* Para visualizar os dois últimos commits em uma única linha:

~~~
git log --oneline -2
~~~

* Para visualizar commits antes de uma data específica:

~~~
git log --before="2023-11-06"
~~~

* Para visualizar commits após uma data específica:

~~~
git log --after="2023-11-06"
~~~

* Para visualizar commits dos últimos 2 dias:

~~~
git log --since="2 days ago"
~~~

* Para buscar commits por autor, utilize:

~~~
git log --author="Thiago"
~~~

* Para obter ajuda sobre o comando log, utilize:

~~~
git help log
~~~

## 9. Comandos Git para Mudanças de Ramificação

Para mudar para um commit específico utilizando o ID do commit:

~~~
git checkout 595cc44
~~~

* Para mudar para a branch "master":

~~~
git checkout master
~~~

## 10. Comandos Git para Renomear Arquivos

Para renomear um arquivo no Git, utilize:

~~~
git mv programa1.html programa3.html
~~~

## 11. Comando Git para Remover Arquivos

Para remover um arquivo do repositório e do stage, utilize o comando git rm:

~~~
git rm programa3.html
~~~

## 12. Comandos Git para Comparação de Mudanças

Para comparar as diferenças entre o que está no stage (área de stage) e o commit HEAD mais recente, utilize o comando:

~~~
git diff --staged
~~~

* Para comparar as diferenças entre um commit específico (substitua *"c76e4d7"* pelo ID do commit desejado) e o diretório de trabalho atual, utilize o comando:

~~~
git diff c76e4d7
~~~

* Para comparar as diferenças entre dois commits (substitua *"595cc44"* e *"8693ce2"* pelos IDs de commit desejados), utilize o comando:

~~~
git diff 595cc44..8693ce2
~~~

*Este comando mostra todas as alterações entre esses dois pontos no histórico de commits. É útil para entender as mudanças ao longo do tempo.*

>Esses comandos de comparação são valiosos para analisar as alterações em seu repositório Git e ajudam a entender as diferenças entre diferentes estados do código. Certifique-se de fornecer os IDs de commit apropriados ao usar esses comandos.


## 13. Comando Git para Alterar a Mensagem de Commit de um Commit Anterior

Para alterar a mensagem de commit de um commit anterior, utilize o comando *git commit --amend -m*:

~~~
git commit --amend -m "Novos comandos para a documentação"
~~~

* Isso permite que você adicione ou modifique a mensagem do commit anterior. É útil quando você percebe que a mensagem do commit precisa ser corrigida ou aprimorada. Certifique-se de substituir "Nova mensagem para o commit" pela mensagem que deseja usar.

>Lembre-se de que, ao usar *git commit --amend*, você está reescrevendo o histórico do commit, portanto, use com cuidado, especialmente se o commit já foi compartilhado com outras pessoas.


## 14. Comandos Git para Restaurar e Resetar Mudanças
Para restaurar um arquivo do stage (área de stage) ao estado anterior no diretório de trabalho, utilize o comando *git restore --staged*:

~~~
git restore --staged programa4.html
~~~

Para resetar o *HEAD (a referência para o commit atual)* para o estado atual do diretório de trabalho, descartando todas as alterações, utilize o comando *git reset* com a opção *--hard*:

~~~
git reset HEAD --hard
~~~

Para resetar o HEAD para o commit anterior, utilize o comando git reset com a opção --hard e HEAD^:

~~~
git reset HEAD^ --hard
~~~

## 15. Adicionando uma outra branch

~~~
git branch funcionalidadeA
~~~

~~~
git checkout - muda de branch
~~~

* Delete de branch antes de realizar merge

~~~
git branch -D funcionalidadeA 
~~~

* Faz a junção de arquivos entre branchs 

~~~
git merge funcionalidadeB
~~~

* Delete de branch depois do merge de arquivos

~~~
git branch -D funcionalidadeA 
~~~

* Git rebase

~~~
git rebase funcionalidadeC
~~~