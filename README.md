# zsh-installation
Zsh installation on ubuntu with agnoster theme

### Install Zsh
```
sudo apt-get update && sudo apt-get install zsh 
```

### Install Oh-my-zsh
```
wget –no-check-certificate https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O ~/.zshrc | sh 
```
> **Note:** Git should be pre-installed for above commands.

### Make ZSH default shell
```
chsh -s /bin/zsh
```
> Now **logout and login** again to see changes.

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
