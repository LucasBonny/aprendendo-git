# Aprendendo Git
Aprendendo a utilizar o versionamento adequado em projetos com o git.

# Aula 1 - Repositório Local e Remoto

Um projeto que é versionado pelo git e conhecido como repositório de versionamento.
Naturalmente, os projetos que utilizam o git, precisam ter um repositório em um servidor remoto, possibilizando a utilização de vários usuários permitindo a colaboração entre eles dentro do projeto.

> [!IMPORTANT]
> O repositório remoto é o repositório que fica armazenado no servidor, e o repositório local é o repositório que fica armazenado no computador do usuário.

# Aula 2 - Primeiro Projeto

## Salvar a versão inicial do projeto
`git init` - Inicializa o repositório local do projeto.

>[!important]
>O repositório local fica armazenado na pasta `.git` dentro da pasta do projeto.

`git status` - Verifica se os arquivos foram adicionados na area de staging.

```bash
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

```

`git add .` - Adiciona todos os arquivos do projeto que foram modificados na area de staging.


`git commit -m "Primeira versão"` - Salva uma nova versão do projeto.

```bash
$ git commit -m "Testando markdown para as aulas"
[main 9507c91] Testando markdown para as aulas
 1 file changed, 71 insertions(+)
```

> [!caution]
> Para garantir que o projeto seja salvo na branch main em seu github, será necessario executar o comando: `git branch -M main`

`git remote add origin git@github.com:usuario/projeto.git` - Associar o repositório local ao repositório remoto.

`git push -u origin main` - Envia a versão inicial do projeto para o repositório remoto.

```bash
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 688 bytes | 688.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:LucasBonny/aprendendo-git.git
   ee91248..9507c91  main -> main
```
# Aula 3 - Um novo commit

Ao modificar um arquivo no projeto, ele precisa ser salvo na area de staging para ser adicionado ao commit.

para verificar se há arquivos modificados na area de staging, execute o comando `git status`

```bash
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
Use o comando `git add .` para adicionar todos os arquivos modificados na area de staging.

Com os arquivos modificados na area de staging, execute o comando `git commit -m "Mensagem do commit"`

```bash
$ git commit -m "Aula 1 - Mostrando Terminal"
[main 7b6746a] Aula 1 - Mostrando Terminal
 1 file changed, 24 insertions(+), 3 deletions(-)
```

Por não ser mais o primeiro commit então o comando `git push` irá enviar o commit para o repositório remoto.

```bash
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 680 bytes | 680.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:LucasBonny/aprendendo-git.git
   0bf8725..7b6746a  main -> main
```