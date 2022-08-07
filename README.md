# Git e Github

Guia prático

# Instalação

https://git-scm.com/download

# Objetivos do estudo

[x] criar pontos na história da produção do projeto 
- git init: iniciar linha do tempo
- git add [file_name]: preparar atualização para linha do tempo (staging area)
- git commit -m "commentários": adicionar ponto na linha do tempo

[x] verificar mudanças feitas no projeto 
- git status: informa estado das alterações no projeto
- git log: visualiza pontos/commits na linha do tempo
- git show [commit_id]: apresenta determinado ponto na linha do tempo

[x] criar/gerenciar branches de projetos
- git branch [branch_name]: criar / listar branches
- git checkout [branch_name]: ativar branch [branch_name]

[x] mesclar branch com master 
- git merge [branch_name]: faz o 'merge' de branch [branch_name] com o branch atualmente ativo

[x] excluir branchqq
- git branch -D [branch_name]: exclui a branch [branch_name]

[x] hospedar o projeto na nuvem do github
No caso, optou-se por utilizar o terminal/ambiente WSL-2 (Windows subsystem for Linux 2) com o Windows 11. Para tal, é necessário instalar a(s) distro(s) (distribuição linux) linux.
1- o comando WSL --install, executado a partir do terminal 'Windows PowerShell' ou do 'Prompt de Comando' (cmd.exe), executados no modo Adminstrador, permite instalar as 'distros' do linux
- wsl --list --online: listar 'distros' disponíveis
- wsl --install -d [Name]: instalar a distro de nome [Name], conforme retornado pelo comando 'wsl --list --online'
- wsl --list --verbose: lista distribuições Linux instaladas e sua versão WSL (se WSL 1 ou WSL 2)
1- instalar/atualizar o git no terminal WSL2: No Ubuntu > sudo apt-get install git.Geralmente o git vem pré-instalado nas diversas distros
- instalar o Git e o Git GUI no windows: https://git-scm.com/download/win
- executar o Git GUI conectá-lo 
- git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"
 