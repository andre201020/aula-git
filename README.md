# Terminal Linux WSL-2 (Windows Subsystem for Linux) com Git acessando Github via GCM no host Windows 11

## Instalar distro/distribuição Linux
Abrir, como administrador, um terminal do Windows: Windows PowerShell ou Prompt de Comando (cmd.exe). No terminal, executar comandos WSL para selecionar e instalar distros do linux - uma ou mais distros podem ser instaladas num mesmo host Windows. 
- `wsl --list --verbose`: listar distribuições linux e versões do WSL - WSL 1 ou 2;
- `wsl --list --online`: listar 'distros' disponíveis online para instalação;
- `wsl --install -d [Name]`: instalar a distro de nome [Name], conforme retornado pelo comando `wsl --list --online`

## Instalação do Git
-Fazer [download do Git]('https://git-scm.com/download');
- instalar/atualizar o Git no terminal linux WSL2: No Ubuntu: `sudo apt-get install git`. Comumente, o Git vem pré-instalado nas diversas distros linux.
- instalar o Git e o Git GUI no windows: https://git-scm.com/download/win
- executar o Git GUI conectando-o com a nuvem do GitHub, autorizando assim as futuras conexões do repositório local do Git com o repositório remoto no GitHub.
- para vincular o terminal linux WSL-2 ao GCM (git credentials manager) no windows, no próprio terminal linux rodar o comando: `git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"`

## Objetivos do estudo

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
