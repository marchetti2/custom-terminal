This is a custom terminal with an Zsh, Oh My Zsh, FiraCode and Dracula.

## Installing Zsh
https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH

after installing, may you should execute this code on terminal
```bash
zsh --version
```
and then received something like:
```bash
zsh 5.3 (x86_64-apple-darwin18.0)
```
## Installing Oh My Zsh
To install Oh My Zsh you must run the following command(you must have the cURL installed to run the command):
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
From now on, all the settings you want to make, use the ~ / .zshrc file and no longer ~ / .bash_profile.

## Using Dracula theme on terminal
https://draculatheme.com/terminal/

## Installing FiraCode
https://github.com/tonsky/FiraCode/releases

## Using Dracula theme on zsh
Let's clone the dracula repo:
```bash
git clone https://github.com/dracula/zsh.git "$ZSH_CUSTOM/themes/dracula-prompt"
```
And creating a symbolic link to oh-my-zsh's theme folder:
```bash
ln -s "$ZSH_CUSTOM/themes/dracula-prompt/dracula.zsh-theme" "$ZSH_CUSTOM/themes/dracula.zsh-theme"
```
to activating theme go to your ~/.zshrc file and set: 
```bash
ZSH_THEME="dracula"
```

## ZSH Plugins

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
```

After this installation, we will open the ~ / .zshrc file again and below the line ### End of ZInit's installer chunk that was automatically added to the file, we add:

```bash
zinit light zdharma/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
```

## Integrated Terminal on VSCode

```bash
"terminal.integrated.shell.osx": "/bin/zsh"
```
