# wsl-linux-env
How to configure a Linux environment using WSL. (Windows 11 recommended)

# First of all
- You'll need to install [`Ubuntu`](https://www.microsoft.com/pt-br/p/ubuntu/9nblggh4msv6) from MicrosoftStore.

# Install zsh + OhMyZsh

# Step 1: zsh

- Install and set up zsh as default kernel
- Execute: `sudo apt install zsh`
- Make it your default shell: `chsh -s $(which zsh)`
- Source: https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH

# Step 2: Oh My Zsh

- Execute `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

# Step 3: plugins (optional):

- Add line below to your `.zshrc` (generally at `\\wsl.localhost\Ubuntu\home\%USER%`)

- `plugins=(git git-flow fast-syntax-highlighting zsh-autosuggestions zsh-completions)`

  # 3.1 zsh-completions
  - Execute `git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions`

  - Add it to `FPATH` in your `.zshrc` by adding the following line before `source "$ZSH/oh-my-zsh.sh"`:
  - `fpath+=${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions/src`
  - Source: https://github.com/zsh-users/zsh-completions#oh-my-zsh

  # 3.2 zsh-autosuggestions
    - Execute `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
    - Source: https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md

  # 3.3 fast-syntax-highlighting
  - Execute `git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git \
           ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting`
  - Source: https://github.com/zdharma-continuum/fast-syntax-highlighting#oh-my-zsh
