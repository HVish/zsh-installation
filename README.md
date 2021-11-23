# zsh-installation
Zsh installation on ubuntu/mac-osx with agnoster theme

### Install Zsh

#### Ubuntu
```
sudo apt-get update && sudo apt-get install zsh
```

#### Mac OSX
```
brew install zsh
```

### Install Oh-my-zsh
**Note:** Git should be pre-installed for following commands.
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" 
```

### Make ZSH default shell
```
chsh -s /bin/zsh
# OR
sudo chsh -s $(which zsh) $(whoami) # useful when logged in with a user having no password
```

### Change theme name in ~/.zshrc 
```
ZSH_THEME="agnoster"
```

### System wide powerline font installation

#### Ubuntu
```
wget https://github.com/Lokaltog/powerline/raw/develop/font/PowerlineSymbols.otf https://github.com/Lokaltog/powerline/raw/develop/font/10-powerline-symbols.conf
sudo mv PowerlineSymbols.otf /usr/share/fonts/
sudo fc-cache -vf
sudo mv 10-powerline-symbols.conf /etc/fonts/conf.d/
```

#### Mac OSX
1. Download powerline font from [here](https://github.com/powerline/fonts/archive/master.zip)
2. Unzip it. Go to fonts-master/UbuntuMono/ and install each of the four TTFs: simply double-click and let Font Book install them for you.
3. Open Terminal, then navigate to Terminal Preferences > Profiles > Font and click the Change button.
4. Select Ubuntu Mono derivative Powerline and set the font size to your liking.

### Reload .zshrc to see changes
```
source ~/.zshrc
```
If above command doesn't work then logout and login again.

### VSCode integrated terminal font issues:
If you are using Ubuntu then add following settings to vscode
```jsonc
{
    "terminal.integrated.fontFamily": "'Ubuntu Mono', 'PowerlineSymbols'", // "'Ubuntu Mono derivative Powerline'" for mac osx
    "terminal.integrated.defaultProfile.osx": "zsh",
    "terminal.integrated.fontSize": 16
}
```
You can refer to: https://github.com/oh-my-fish/theme-bobthefish/issues/125
