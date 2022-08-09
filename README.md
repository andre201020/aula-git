# Terminal Linux WSL (Windows Subsystem for Linux) com Git acessando Github via GCM (Git Credential Manager) executando no host Windows 11

## Instalação do Linux no WSL - Windows Subsystem for Linux
1. abrir terminal Windows (no modo administrador): **Windows PowerShell** ou **Prompt de Comando (cmd.exe)**
2. os comandos `WSL` abaixo, são usados para gerenciar terminais linux WSL: 
- `wsl --list --verbose`: listar distribuições linux instaladas no host;
- `wsl --list --online`: listar **distros** linux disponíveis online para instalação;
- `wsl --install -d [Name]`: instalar distro [Name], conforme retornado por `wsl --list --online`. Uma ou mais distros podem ser instaladas num host Windows.
Mais comandos WSL em [Comandos básicos para o WSL | Microsoft Docs](https://docs.microsoft.com/pt-br/windows/wsl/basic-commands)

## Instalação/configuração do Git
1. instalar/atualizar o Git no terminal linux WSL. No Ubuntu, o comando `sudo apt-get install git` faz o download e a instalação ou atualização do git. Geralmente o Git já vem pré-instalado nas distros do linux.
2. fazer [download do Git for Windows](https://git-scm.com/download/win).
3. instalar o Git e o Git GUI no windows 
4. executar o Git GUI para conectar na nuvem do GitHub, autorizando futuras conexões do repositório local do Git ao repositório remoto do GitHub.
5. para vincular o terminal linux WSL-2 ao serviço GCM (git credentials manager) do windows, do terminal linux rodar o comando: `git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"`.

## Comandos básicos do Git
Criar pontos na história da produção do projeto:
- `git init`: iniciar linha do tempo
- `git add [file_name]`: preparar atualização para linha do tempo (staging area)
- `git commit -m "commentários"`: adicionar ponto na linha do tempo

Verificar mudanças feitas no projeto:
- `git status`: informa estado das alterações no projeto
- `git log`: visualiza pontos/commits na linha do tempo
- `git show [commit_id]`: apresenta determinado ponto na linha do tempo

Criar/gerenciar branches de projetos:
- `git branch [branch_name]`: criar / listar branches
- `git checkout [branch_name]`: ativar branch [branch_name]

Mesclar branch com master:
- `git merge [branch_name]`: faz o 'merge' de branch [branch_name] com o branch atualmente ativo

Excluir branch:
- `git branch -D [branch_name]`: exclui a branch [branch_name]

Hospedar projeto na nuvem do github:
