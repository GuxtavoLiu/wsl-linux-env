# wsl-linux-env
How to configure a Linux environment using WSL. (Windows 11 recommended)


# Manual de instalação zsh + ohmyzsh

# Passo 1: Instalar o zsh
Install and set up zsh as default
If necessary, follow these steps to install Zsh:

Execute: `sudo apt install zsh`


Verify installation by running `zsh --version`. Expected result: zsh 5.8 or more recent.

Make it your default shell: `chsh -s $(which zsh)`
Test that it worked with `echo $SHELL`. Expected result: /bin/zsh or similar.

Test with `$SHELL --version`. Expected result: 'zsh 5.8' or similar

# Passo 2: Instalar o Oh My Zsh
Execute `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

# Passo 3 (opcional) Plugins:
 - Adicionar a linha abaixo ao .zshrc

 - `plugins=(git git-flow fast-syntax-highlighting zsh-autosuggestions zsh-completions)`

# 3.1 Instalar os plugins 
  # zsh-completions
  Clone the repository inside your oh-my-zsh repo:
  
  `git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions`


Add it to FPATH in your .zshrc by adding the following line before source "$ZSH/oh-my-zsh.sh":

  `fpath+=${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions/src`
  
  
- zsh-autosuggestions
  
  https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md
  `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

- fast-syntax-highlighting

https://github.com/zdharma-continuum/fast-syntax-highlighting#oh-my-zsh
`git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git \
  ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting`
