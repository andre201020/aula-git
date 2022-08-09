# Terminal Linux WSL (Windows Subsystem for Linux) com Git acessando Github via GCM (Git Credential Manager) executando no host Windows 11

## Instalação do Linux no WSL - Windows Subsystem for Linux
1. abrir terminal Windows (no modo administrador): **Windows PowerShell** ou **Prompt de Comando (cmd.exe)**
2. os comandos `WSL` abaixo, são usados para gerenciar terminais linux WSL: 
- `wsl --list --verbose`: listar distribuições linux instaladas no host;
- `wsl --list --online`: listar **distros** linux disponíveis online para instalação;
- `wsl --install -d [Name]`: instalar distro [Name], conforme retornado por `wsl --list --online`. Uma ou mais distros podem ser instaladas num host Windows.
Mais comandos WSL em [Comandos básicos para o WSL | Microsoft Docs](https://docs.microsoft.com/pt-br/windows/wsl/basic-commands)

## Instalação e configuração mínima do Git
1. instalar/atualizar o Git no terminal linux do WSL. 
Em distribuições Debian-based como Ubuntu, o comando `sudo apt install git-all` faz download e instalação/atualização do git. Geralmente, o git vem pré-instalado nas distros linux.
2. fazer [download do Git for Windows](https://git-scm.com/download/win), instalando-o juntamente com o Git GUI no windows - o processo de instalação apresenta algumas opções que poderão ser mantidas no seu valor padrão ou alteradas. 
3. executar o Git GUI para conectar na nuvem do GitHub, autorizando futuras conexões do repositório local do Git ao repositório remoto do GitHub.
4. para vincular o terminal linux-WSL ao serviço GCM (git credentials manager) do windows, executar o comando no próprio terminal linux-WSL: `git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/bin/git-credential-manager-core.exe"`.
5. configurar nome e email do usuário git, que são necessários nos `commits`: 
- `git config --global user.name "Usuário-Nome"`
- `git config --global user.email usuário@dominio.com`
6. Mais usos do comando de configuração do Git [`git config ...`](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

### Usos dos parâmetros de escopo do comando `git config  [--local|--global|--system]`
- parâmetro `--global`, utilizando `git config --global...`, define configurações do git para o escopo do usuário ativo do linux (`whoami` retorna usuário ativo no linux) e essa configuração é mantida no arquivo `~/.gitconfig` (no caso do Ubuntu);
- já o parâmetro `--system` (`git config --system...`) usa escopo do sistema, alterando o arquivo de configuração `/etc/gitconfig` que precisa de privilégio **administrativo** ou **superuser**;
- enquanto o parâmetro `--local`, que é **default**, usa o escopo mínimo que é o próprio diretório Git, mantendo a configuração no arquivo .git/config.

## Comandos básicos do Git
Criar pontos na história da produção do projeto:
- `git init`: iniciar linha do tempo no diretório ativo
- `git add [file_name]`: preparar atualização para linha do tempo (staging area)
- `git commit -m "commentários"`: adicionar ponto na linha do tempo

Verificar mudanças feitas no projeto:
- `git status`: informa estado das alterações no projeto
- `git log`: visualiza pontos/commits na linha do tempo
- `git show [commit_id]`: apresenta determinado ponto na linha do tempo

Criar/gerenciar branches de projetos:
- `git branch [branch_name]`: criar / listar branches
- `git checkout [branch_name]`: ativar branch [branch_name]
- `git branch -D [branch_name]`: exclui a branch [branch_name]

Mesclar branch com master:
- `git merge [branch_name]`: faz o 'merge' de [branch_name] com o branch ativo

Hospedar projeto na nuvem do github:
- `git push ...`

[Documentação do Git](https://git-scm.com/doc)