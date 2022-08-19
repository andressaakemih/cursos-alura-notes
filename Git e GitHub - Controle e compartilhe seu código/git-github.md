# Git e GitHub: repositório, commit e versões

* Assunto: Git
* Criado: July 29, 2022 3:01 PM
* Finalizado: Yes
* Materiais: https://cursos.alura.com.br/course/git-github-repositorio-commit-versoes/task/106062
* Plataforma: Alura

## 01 - Conta no GitHub

01 - **Para que serve o GitHub?**

Uma equipe de pessoas desenvolvedoras está trabalhando em um projeto para realizar mudanças na plataforma de cursos da Alura. Uma pessoa está fazendo uma melhoria no código, outra precisa corrigir um bug no sistema e outra vai alterar as cores do dashboard.

Essas mudanças estão ocorrendo simultaneamente e, para agilizar o desenvolvimento, os devs querem ter acesso ao código atualizado com as mudanças feitas pela equipe em tempo real.

O que você pode fazer para solucionar essa questão?

→ *Utilizar o GitHub, pois ele serve para unificar as mudanças de toda a equipe em um único local, denominado repositório.*

→ *Alternativa correta! Isso mesmo, com o GitHub, a equipe de devs poderá gerenciar muito mais facilmente as alterações no projeto. Um repositório é basicamente um diretório onde ficarão reunidos todos os arquivos do projeto e poderá ser acessado por todas as pessoas da equipe.*

## 02 - Commit, VSCode e equipe

02 - **Realizando um commit**

O commit é uma ação muito importante do Git para nos ajudar no controle da versão do nosso projeto. Um commit pode ser considerado como um marco ao longo do cronograma de um projeto.

Sabendo disso, quando realizamos um commit, estamos:

→ *Adicionando as alterações mais recentes do projeto.*

→ *Alternativa Correta! Um commit guarda o estado do seu projeto naquele momento.*

## 03 - Trabalhando localmente

```powershell
Clonar o repositorio do GitHub
-> git clone https://github.com/andressaakemih/alura-git.git

Verificar o log
-> git log

Verificar o log em uma linha
-> git log --oneline

Baixar a atualização do repositorio
-> git pull

Verificar o estado do projeto
-> git status

Adicionando as alterações somente do index com a mensagem do commit
-> git commit index.html -m "adicionando uma lista"

Configurando infos (Nome e E-mail)
-> git config --global --edit

Enviando as alterações para o GitHub
-> git push

Adicionando as alterações de todos os arquivos alterados
-> git commit . -m "adicionando outra lista"

Voltando uma versão anterior (todos os arquivos)
-> git restore --source 9d0f8b7 .

Mais informações do commit
-> git log -p

Pesquisando infos do autor do commit
-> git log --author="user_name"

Pesquisando infos por data
-> git log --since=1.month.ago --until=1.day.ago

```

03 - **Comando git push**

O comando git push é usado quando você deseja enviar as alterações realizadas no seu repositório local para um repositório remoto.

Qual a sequência CORRETA de comandos ao enviar as alterações de um repositório local para um repositório remoto?

```powershell
*git add .
git commit -m "mensagem de commit"
git push origin main*
```

→  *Alternativa correta! Para enviarmos as alterações de um **repositório local**
 para um **repositório remoto**  é preciso adicionar os arquivos com o `git add .`
 e depois fazer o commit com `git commit` . Feito isso é possível  enviar/empurrar as alterações para o repositório remoto utilizando o `git push origin main`*

## 04 - Adicionando arquivos

04 - **Navegando no tempo**

Você fez quatro commits em seu código HTML: Adicionando Title, Adicionando imagem de fundo, Adicionando tabela e Adicionando footer, mas os três últimos commits não foram aprovados por seu supervisor. Então, você precisa voltar ao ponto inicial do projeto. Qual o comando que você precisa utilizar para navegar no passado?

Com base no que vimos em aula, analise as alternativas abaixo e marque apenas a correta:

→ *Usamos o comando restore para voltar exatamente ao ponto que inicial do projeto.*

→ *Usamos o comando Restore informando o ID do primeiro commit depois da flag --source. Te convido a ler mais sobre Restore [nesse artigo da Alura](https://www.alura.com.br/artigos/git-os-novos-comandos-git-restore-e-git-switch).*

## 05 - Ramificações e merge

```powershell
Criando uma branch
-> git checkout -b desenvolvimento

Entrando na branch
-> git switch main

Mandando as alterações pela branch desenvolvimento
-> git push origin desenvolvimento

Mostra as branchs
-> git branch

Mandar para a main (merge)
-> git merge desenvolvimento

Mandar alterações pela branch main
-> git push origin main
```

05 - **Merge de branches**

Estamos trabalhando com duas branches: a branch `main` e a branch `title`. Fizemos várias alterações na branch `title`, mas, agora, queremos trazer tudo o que está na `title` para a `main`. Como podemos fazer isso?

→ *Utilizamos os comandos: `git switch main` e `git merge title`.*

→ *Alternativa correta! Isso aí! Desta forma com o `git switch` voltamos pra branch principal e depois fazemos o `merge` colocando tudo o que estava na `branch title` na `branch main`.*