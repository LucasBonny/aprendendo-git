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

`git add .` - Adiciona todos os arquivos do projeto na area de staging.

`git status` - Verifica se os arquivos foram adicionados na area de staging.

`git commit -m "Primeira versão"` - Salva uma nova versão do projeto.

> [!important]
> Para garantir que o projeto seja salvo na branch main em seu github, será necessario executar o comando: `git branch -M main`

`git remote add origin git@github.com:usuario/projeto.git` - Associar o repositório local ao repositório remoto.

`git push -u origin main` - Envia a versão inicial do projeto para o repositório remoto.