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

[x] criar branch/ramo do projeto principal
- git branch [branch_name]: lista/cria branch
- git checkout [branch_name]: alterna entre branches

[x] mesclar branch com master 
- git merge [branch_name]: faz o merge de [branch_name] com o branch atual

[x] excluir branch
- git branch -D [branch_name]: exclui a branch [branch_name]

[x] hospedar o projeto na nuvem do github, utilizando terminal/ambiente WSL-2 (Windows subsystem for Linux 2) com o Windows 11 
- instalar/atualizar o git no terminal WSL2: No Ubuntu > sudo apt-get install git. Geralmente o git vem pré-instalado nas diversas distros
- instalar o Git e o Git GUI no windows: https://git-scm.com/download/win
- executar o Git GUI conectá-lo 
- git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"
 