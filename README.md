# Personal Terminals Configuration

A comprehensive collection of shell configurations for PowerShell, Bash, and Zsh with Starship integration for a consistent and powerful terminal experience across different platforms.

## 🚀 Features

- **Multi-Shell Support**

  - PowerShell with extensive utility functions and customizations
  - Bash with oh-my-bash integration
  - Zsh with oh-my-zsh integration
  - Starship prompt configuration for all shells

- **PowerShell Enhancements**

  - Automatic profile updates
  - Rich command completion
  - Syntax highlighting
  - History search
  - Git integration
  - Unix-like command aliases
  - File and directory management utilities
  - System monitoring tools

- **Bash & Zsh Features**

  - oh-my-bash/oh-my-zsh integration
  - Custom themes and plugins
  - Git integration
  - Command completion
  - History management

- **Starship Configuration**
  - Customized prompt for all shells
  - Rich programming language support
  - Git status integration
  - Cloud platform integration (AWS, Azure, GCloud)
  - System resource monitoring
  - Custom icons and formatting

## 🛠️ Technologies

- PowerShell 7+
- Bash
- Zsh
- Starship
- Oh-My-Bash
- Oh-My-Zsh
- Terminal Icons
- PSReadLine

## 📦 Installation

### Prerequisites

- PowerShell 7+ (for PowerShell configuration)
- Bash or Zsh shell
- [Starship](https://starship.rs/) cross-shell prompt
- [Oh-My-Bash](https://github.com/ohmybash/oh-my-bash) (for Bash)
- [Oh-My-Zsh](https://ohmyz.sh/) (for Zsh)
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads) - Required for proper icon display

#### Installing JetBrainsMono Nerd Font

1. Download JetBrainsMono Nerd Font from [Nerd Fonts website](https://www.nerdfonts.com/font-downloads)
2. Extract the downloaded archive
3. Install the font:
   - **Windows**: Right-click on each .ttf file and select "Install", or select all files and install them at once
   - **macOS**: Double-click each .ttf file and click "Install Font"
   - **Linux**: Copy the .ttf files to `~/.local/share/fonts/` and run `fc-cache -fv`
4. Configure your terminal to use "JetBrainsMono Nerd Font" as the default font

### Setup Steps

1. **Clone the Repository**

   ```powershell
   git clone https://github.com/yourusername/personal-terminals.git
   ```

2. **PowerShell Configuration**

   ```powershell
   # Copy PowerShell profile
   Copy-Item "pwsh/Microsoft.PowerShell_profile.ps1" $PROFILE.CurrentUserAllHosts

   # Install required modules
   Install-Module -Name Terminal-Icons -Scope CurrentUser
   ```

3. **Bash Configuration**

   ```bash
   # Backup existing configuration
   cp ~/.bashrc ~/.bashrc.backup

   # Copy new configuration
   cp bash/.bashrc ~/.bashrc
   cp -r bash/StarShip ~/.config/starship
   ```

4. **Zsh Configuration**

   ```bash
   # Backup existing configuration
   cp ~/.zshrc ~/.zshrc.backup

   # Copy new configuration
   cp zsh/.zshrc ~/.zshrc
   ```

5. **Starship Configuration**

   ```bash
   # Create Starship config directory
   mkdir -p ~/.config/starship

   # Copy Starship configuration
   cp bash/StarShip/starship.toml ~/.config/starship/starship.toml
   ```

## 🔧 Usage

### PowerShell Functions

- `Update-Profile`: Check for and apply profile updates
- `Update-PowerShell`: Update PowerShell to the latest version
- `Clear-Cache`: Clear system cache
- `Edit-Profile`: Open profile in default editor
- `uptime`: Display system uptime
- Many Unix-like command aliases (ls, grep, touch, etc.)

### Bash/Zsh Features

- Custom prompt with Starship integration
- Git status information
- Directory navigation shortcuts
- Command completion

### Starship Customization

The Starship prompt is configured to show:

- Operating system indicator
- Current directory
- Git branch and status
- Programming language versions
- Cloud platform status
- Command execution time

## 🧪 Testing

The repository includes various shell scripts and configurations. Test new changes in a separate shell session before applying them to your main configuration.

```powershell
# Test PowerShell profile
pwsh -NoProfile -Command {
    . ./pwsh/Microsoft.PowerShell_profile.ps1
}
```

## 📝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Starship](https://starship.rs/) for the cross-shell prompt
- [Oh-My-Bash](https://github.com/ohmybash/oh-my-bash) community
- [Oh-My-Zsh](https://ohmyz.sh/) community
- PowerShell community for various utility functions and inspiration
