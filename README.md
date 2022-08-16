# Install_and_Config_Zsh
Setup and Configure Zsh + Oh my Zsh + Powerlevel10k + Dracula theme with auto-suggestions and syntax-higlighting

# Install zsh in Ubuntu using an apt package manager
```
sudo apt install zsh -y
```

# Set Zsh as default shell
chsh -s /usr/bin/zsh
In case of an error do the following:
```
sudo vim ~/.bashrc
```
add the following:
```
if [ $?prompt ]; then
  exec /usr/bin/zsh -l
  export SHELL=/usr/bin/zsh
fi
```
#  Install oh my zsh using curl
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
# Use agnoster zsh theme
```
sudo vim ~/.zshrc
Edit from ZSH_THEME="robbyrussell" to ZSH_THEME="agnoster" 
# see https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster
```

# Install powerline
```
sudo apt-get install fonts-powerline
```

# Install powerlevel10k for Oh my zsh
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

# Set ZSH_THEME
```
sudo vim ~/.zshrc
ZSH_THEME="powerlevel10k/powerlevel10k"
```

# Cocnfigure p10k
```
p10k configure
```

#  Install dconf-cli
```
sudo apt-get install dconf-cli
```

# clone repo
```
git clone https://github.com/dracula/gnome-terminal
cd gnome-terminal
```
Right click in the terminal, then choose preferences. In preferences, choose add profiles, fill the new profile name i.e. dracula.
In the Colors tab, uncheck the ‘Use colors from system theme’ in Text and Background Color. Then, close the preferences.

Install:
```
./install.sh
```

# Install plugins (zsh-autosuggestions and zsh-syntax-highlighting)
Download zsh-autosuggestions :
```
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions 
```

Download zsh-syntax-higlighting :
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

# edit
```
sudo vim ~/.zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```



REFERENCE:
```
https://github.com/romkatv/powerlevel10k
```



