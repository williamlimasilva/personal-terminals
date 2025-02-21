# Starship: O Prompt do Futuro para Desenvolvedores

## Introdução

Para muitos desenvolvedores, o terminal é um ambiente essencial de trabalho. Porém, com o tempo, os terminais tradicionais podem parecer monótonos e sem vida. Se você está em busca de uma maneira de personalizar e otimizar sua experiência no terminal, o Starship é a solução ideal. Este prompt de shell moderno não só oferece uma interface rápida e responsiva, como também permite personalização avançada, com suporte a ícones e estilos visuais, além de integração com várias tecnologias. Neste artigo, vamos explorar o conceito, como instalar, configurar e até desinstalar o Starship.

## O que é o Starship?

O Starship é um prompt de shell altamente personalizável e rápido, projetado para desenvolvedores. Ele funciona em diversas plataformas, como Linux, macOS e Windows, e se integra com shells como Bash, Zsh, Fish e PowerShell. Ao contrário dos prompts tradicionais, o Starship exibe informações relevantes diretamente no prompt, como o status do Git, a versão do Node.js, Python, Java, entre outros, de uma forma limpa e eficiente. Ele também permite o uso de ícones e glyphs para enriquecer a visualização de informações.

## Características do Starship

- **Multiplataforma**: Funciona em Linux, macOS e Windows.
- **Configuração fácil**: Arquivo de configuração simples em TOML.
- **Personalização avançada**: Adicione módulos personalizados e ajuste cores, estilos e ícones.
- **Desempenho**: Rápido e eficiente, sem comprometer a performance do terminal.

## Instalando o Starship

### Passo 1: Instalação no Linux

Para instalar o Starship em sistemas baseados em Linux, você pode usar o gerenciador de pacotes do seu sistema. Vamos ver como fazer isso no Ubuntu:

1. Abra o terminal.
2. Execute o seguinte comando para baixar e instalar o Starship:

   ```sh
   curl -sS https://starship.rs/install.sh | sh
   ```

3. Após a instalação, adicione a linha abaixo ao arquivo de configuração do seu shell (`~/.bashrc`, `~/.zshrc`, etc.):

   ```sh
   eval "$(starship init zsh)"  # Para Zsh
   eval "$(starship init bash)"  # Para Bash
   ```

4. Reinicie o terminal ou recarregue o arquivo de configuração com o comando:

   ```sh
   source ~/.zshrc  # Ou ~/.bashrc
   ```

### Passo 2: Instalação no macOS

No macOS, o processo é muito semelhante ao Linux. Caso você tenha o Homebrew instalado, basta rodar o comando:

```sh
brew install starship
```

Depois, adicione o código de inicialização no seu arquivo de configuração do shell (por exemplo, `~/.zshrc`):

```sh
eval "$(starship init zsh)"  # Para Zsh
```

Reinicie o terminal ou recarregue a configuração:

```sh
source ~/.zshrc
```

### Passo 3: Instalação no Windows

#### Instalação via Winget

No Windows, o winget é uma das formas mais simples de instalar o Starship. O winget é o gerenciador de pacotes da Microsoft e está disponível no Windows 10 (versão 1809 ou superior) e no Windows 11.

Para instalar o Starship no Windows via winget, basta seguir os passos abaixo:

1. Abra o Prompt de Comando ou PowerShell.
2. Execute o comando de instalação:

   ```sh
   winget install --id Starship.Starship -e
   ```

Isso instalará a versão mais recente do Starship disponível no repositório do winget.

3. Configure o Starship:

   Após a instalação, adicione a linha de inicialização do Starship ao seu arquivo de configuração do shell.

   Para PowerShell: Adicione a seguinte linha ao seu perfil do PowerShell (`$PROFILE`):

   ```sh
   Invoke-Expression (&starship init powershell)
   ```

   Para CMD: Adicione a seguinte linha ao seu arquivo `cmd.ini`:

   ```sh
   @echo off
   call :starship
   goto :eof
   :starship
   set STARSHIP_INIT=1
   for /f "delims=" %%i in ('starship init cmd') do set "%%i"
   ```

4. Reinicie o terminal ou recarregue o arquivo de configuração:

   Para o PowerShell, você pode executar:

   ```sh
   source $PROFILE
   ```

   Para o CMD, basta abrir um novo terminal.

### Passo 4: Instalação Manual (Caso não use winget)

Caso prefira não utilizar o winget ou precise de uma instalação manual, basta seguir as instruções na [documentação oficial do Starship](https://starship.rs/guide/#%F0%9F%9A%80-installation) para outros métodos de instalação.

## Configurando o Starship

Uma das maiores vantagens do Starship é a sua personalização. Para configurar o Starship, basta editar o arquivo de configuração `~/.config/starship.toml`. Vamos explorar as opções de configuração mais comuns.

### 1. Habilitando ou Desabilitando Módulos

O Starship possui módulos que exibem informações úteis, como status do Git, versão do Python, entre outros. Você pode ativar ou desativar esses módulos de acordo com suas preferências.

Exemplo:

```toml
[git_branch]
disabled = false  # Ativa a exibição do branch do Git

[package]
disabled = true  # Desativa a exibição da versão do gerenciador de pacotes
```

### 2. Personalizando o Ícone do Módulo

Você pode personalizar os ícones utilizados pelo Starship. Por exemplo, se quiser exibir o ícone de Java:

```toml
[java]
symbol = "󰬷"  # Ícone Java
style = "bold yellow"
```

Esse ícone será exibido sempre que o Starship detectar um projeto Java no diretório.

### 3. Alterando o Estilo do Prompt

Além dos ícones, você pode personalizar as cores e o estilo do prompt. Aqui está um exemplo para o módulo de status do Git:

```toml
[git_status]
symbol = "󰇐"  # Ícone de Git
style = "bold green"
```

### 4. Adicionando um Novo Line Break

Se você deseja adicionar um espaço extra entre as linhas do prompt para melhorar a legibilidade, basta ativar a opção `add_newline`:

```toml
add_newline = true
```

## Ícones Personalizados com Glyphs

Uma das grandes vantagens do Starship é o suporte a glyphs (ícones especiais) e Material Design Icons (MDI). Esses ícones tornam seu prompt mais informativo e visualmente atraente.

Por exemplo, o ícone 󰬷 para Java ou 󰠷 para Python pode ser copiado diretamente do site de Material Design Icons e adicionado ao seu arquivo de configuração.

```toml
[java]
symbol = "󰬷"  # Ícone Java
style = "bold yellow"
```

## Desinstalando o Starship

Se, por algum motivo, você decidir desinstalar o Starship, o processo é bem simples.

### Linux e macOS

Se você instalou via curl, basta executar:

```sh
rm -rf ~/.cargo
```

Além disso, remova a linha de inicialização do seu arquivo de configuração do shell.

### Windows

Se você usou o winget, execute:

```sh
winget uninstall --id Starship.Starship
```

Caso tenha utilizado o Chocolatey ou o Scoop, basta usar os respectivos comandos de desinstalação.

## Conclusão

O Starship é uma ferramenta poderosa para quem deseja um terminal mais eficiente e visualmente atraente. Sua fácil instalação, configuração e suporte a ícones personalizados tornam-no uma excelente escolha para desenvolvedores que buscam produtividade e personalização. Além disso, o desempenho rápido do Starship garante que seu terminal continue leve, mesmo com várias informações sendo exibidas.

Com este guia, esperamos que você consiga instalar, configurar e personalizar o Starship de acordo com suas necessidades. O terminal nunca mais será o mesmo!

## Fonte

[Starship](https://starship.rs/)
