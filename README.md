# Preparação

## Instalação

Para instalar o Git entre em: https://git-scm.com/downloads
e instale de acordo com sua máquina.

## Como criar uma chave

Para criar uma chave, você precisará entrar na sua conta do <a href="https://github.com">Github</a> (Caso não tenha, será necessário criar), clicar em "<a href="https://github.com/settings/apps">  Developer settings </a>", depois clicar em "Personal access tokens" e logo após em Tokens (classic), clique Nomeie a chave em "Generate new token" e logo após em "Generate new token (classic)". Nomeie a chave, coloque quanto tempo deseja que a chave fique ativa e selecione as permissões de acesso que essa chave terá.

## Colocando a chave de acesso

Caso esteja no Windows abra o "Gerenciador de Credenciais", clique em "Credenciais do Windows", logo após, clique em "Adicionar uma credencial genérica".

Em "Endereço de rede ou na Internet" coloque: "git:https://github.com"

Em "Nome de Usuário" coloque o mesmo nome que você colocou no seu GitHub (Ex: BrunoSerpa)

Em "Senha" coloque sua chave de aceso.


# Comandos Básicos

## Conectando um Repositório do Git com o Local

Crie uma pasta e encaminhe um "Prompt de Comando" para ela (Uma maneira rápida de se fazer isso é abrindo através do "Explorador de Arquivos" a pasta, clicar na parte superior referente ao caminho até a pasta e digitar: cmd).

Digite no "Prompt de Comando": git init (isso criará uma pasta oculta, caso não apareça clique em "exibir", logo após em "Itens Ocultos").

<h4 style="color: yellow">Obs: Caso o repositório já exista no github utilizasse o comando: "git clone linkDoRepositório" (Isso criará uma pasta com os arquivos, caso não queira criar uma pasta insira o comando: "git clone linkDoRepositório ." (ex: git clone https://github.com/BrunoSerpa/Aprendendo-a-usar-GIT .) </h4>

## Configurando O Git

Após criar uma pasta git através do comando "git init" ou "git clone" o git deverá ser config com o nome e o email do GitHub. Insira os comandos:

-git config --local user.name "seuNome" (Ex: git config --local user.name "BrunoSerpa")

-git config --local user.email "seuEmail" (Ex: git config --local user.email "serpabruno2005@gmail.com")

## Trocando de Master para Main
para trocar para main, insira: git checkout -b main

## Adicionando Arquivos
Antes de adicionar qualquer arquivo é recomendado dar um git status, para visualisar o que precisa adicionar e visualizar o que precisará ser enviado para o repositório.
Insira o comando: git add arquivoAdicionado (Ex: git add README.md). logo após será necessário adicionar um comentário, insira o comando: git commit -m "SeuComentário" (Ex: git commit -m "Iniciei o README.md")

Após isso insira o comando: git push origin main (ou master, depende de você fazer o git checkout)

<h4 style="color: yellow">Obs: Se você não utilizou o comando "git clone" será necessário utilizar o comando "git remote add origin" antes do git push (Ex: git remote add origin https://github.com/BrunoSerpa/Aprendendo-a-usar-GIT)</h4>

# Erros

## Conflito entre repositório Local e Remoto

Isso acontece quando os arquivos do repositório Local não coincidem com o arquivos do repositório remoto, pois uma alteração do remoto feita no repositório remoto não foi visualizada no reporitório local. Para resolver isso insira os comandos:

git pull origin main (Isso fará uma comparação interna entre os arquivos)

git merge --abort

git checkout origin/main (Isso voltará o arquivo como estava antes do "git pull"). Após isso crie uma cópia


git merge origin/main (Isso fará a alteração do repositório remoto.)

git checkout main. (Isso verá se foi realizado alguma alteração no repositório remoto)

Após esses dois comandos, compare ambos os arquivos e altere o que deseja alterar. Após isso os mesmos passos em "Adicionando um Arquivo"