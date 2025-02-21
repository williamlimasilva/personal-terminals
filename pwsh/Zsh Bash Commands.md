# 📜 Lista de Comandos Zsh/Bash

## 📂 Manipulação de Arquivos e Diretórios

- `ls` → Lista arquivos e diretórios
- `ls -la` → Lista todos os arquivos, incluindo ocultos, com detalhes
- `cd <dir>` → Navega até um diretório
- `pwd` → Mostra o diretório atual
- `mkdir <nome>` → Cria um diretório
- `rm <arquivo>` → Remove um arquivo
- `rm -rf <dir>` → Remove um diretório e tudo dentro dele
- `cp <origem> <destino>` → Copia arquivos/diretórios
- `mv <origem> <destino>` → Move/renomeia arquivos/diretórios
- `find <caminho> -name "<padrão>"` → Busca arquivos pelo nome

---

## 📜 Leitura de Arquivos

- `cat <arquivo>` → Exibe o conteúdo de um arquivo
- `tac <arquivo>` → Exibe o conteúdo ao contrário
- `less <arquivo>` → Exibe arquivo paginado
- `head -n <N> <arquivo>` → Exibe as primeiras N linhas
- `tail -n <N> <arquivo>` → Exibe as últimas N linhas

---

## 🔎 Busca e Filtros

- `grep "<texto>" <arquivo>` → Procura um texto dentro de um arquivo
- `grep -i "<texto>" <arquivo>` → Busca ignorando maiúsculas/minúsculas
- `grep -r "<texto>" <dir>` → Busca recursivamente no diretório
- `awk '{print $1, $3}' <arquivo>` → Manipula colunas de um arquivo
- `sed 's/velho/novo/g' <arquivo>` → Substitui texto em um arquivo

---

## 🛠 Permissões e Propriedades

- `chmod +x <arquivo>` → Torna um arquivo executável
- `chmod 755 <arquivo>` → Define permissões (dono rwx, grupo r-x, outros r-x)
- `chown user:grupo <arquivo>` → Muda o dono de um arquivo

---

## 🖥 Processos e Monitoramento

- `ps aux` → Lista todos os processos
- `top` ou `htop` → Exibe processos em tempo real
- `kill <PID>` → Encerra um processo pelo ID
- `kill -9 <PID>` → Mata um processo forçadamente
- `pkill -f "<nome>"` → Mata processos pelo nome

---

## 🌍 Rede

- `ping <host>` → Testa conexão com um host
- `curl <URL>` → Faz requisição HTTP
- `wget <URL>` → Baixa um arquivo
- `netstat -tulnp` → Lista portas abertas

---

## 🛠 Gerenciamento de Pacotes

### Ubuntu/Debian

- `apt update && apt upgrade` → Atualiza pacotes
- `apt install <pacote>` → Instala um pacote
- `apt remove <pacote>` → Remove um pacote

### Arch Linux

- `pacman -Syu` → Atualiza pacotes
- `pacman -S <pacote>` → Instala um pacote
- `pacman -R <pacote>` → Remove um pacote

### MacOS (Homebrew)

- `brew install <pacote>` → Instala um pacote
- `brew upgrade` → Atualiza pacotes

---

## 🎛 Outros Comandos Úteis

- `history` → Exibe histórico de comandos
- `alias gs="git status"` → Cria um atalho para um comando
- `unalias gs` → Remove um alias
- `echo "texto"` → Exibe um texto na saída
- `whoami` → Exibe o usuário logado
- `uptime` → Mostra há quanto tempo o sistema está ligado
- `date` → Exibe a data atual
