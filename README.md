# zsh-installation
Zsh installation on ubuntu with agnoster theme

### Install Zsh
```
sudo apt-get update && sudo apt-get install zsh 
```

### Install Oh-my-zsh
**Note:** Git should be pre-installed for following commands.
```
wget –no-check-certificate https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O ~/.zshrc | sh 
```

### Make ZSH default shell
```
chsh -s /bin/zsh
```

### Change theme name in ~/.zshrc 
```
ZSH_THEME="agnoster"
```

### System wide powerline font installation
```
wget https://github.com/Lokaltog/powerline/raw/develop/font/PowerlineSymbols.otf https://github.com/Lokaltog/powerline/raw/develop/font/10-powerline-symbols.conf
sudo mv PowerlineSymbols.otf /usr/share/fonts/
sudo fc-cache -vf
sudo mv 10-powerline-symbols.conf /etc/fonts/conf.d/
```
### Reload .zshrc to see changes
```
source ~/.zshrc
```
If above command doesn't work then logout and login again.

### VSCode integrated terminal font issues:
If you are using Ubuntu then add following settings to vscode
```json
{
    "terminal.integrated.fontFamily": "'Ubuntu Mono', 'PowerlineSymbols'", // "'Ubuntu Mono derivative Powerline'" for mac osx
    "terminal.integrated.defaultProfile.osx": "zsh",
    "terminal.integrated.fontSize": 16
}
```
You can refer to: https://github.com/oh-my-fish/theme-bobthefish/issues/125
