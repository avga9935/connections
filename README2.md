## Introduction
In this file we are going to learn how to setup and install zsh and myzsh in WSL.

At first open Windows Powershell as Admin and install WSL which will help to install ubuntu(WSL) using :
```
bash
wsl --install
wsl --install -d ubuntu
```
Now it will ask for restart, so restart computer and now in search bar search for ubuntu and open it.
Now it will ask to set Username & Password

Now install zsh using:
```
bash
sudo apt update
sudo apt install zsh
```

Now before installing oh my myzsh change script from bash to zsh using:
```
bash
chsh -s $(which zsh)
```
Now logout from ubuntu usin "EXIT" and log back in (Restart ubuntu app)

Now Install oh my myzsh using :
```
bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
If we want to make any changes to the zsh realted to plugin or anything (config file of zsh) is under "~/.zshrc"
## Install Plugins (Optional):
Oh My Zsh supports various plugins that enhance its functionality. You can enable plugins by adding them to your ~/.zshrc file.
To enable the git and sudo plugins, run following command :
```
bash
plugins=(git sudo)
```
## Reload Zsh:
To apply your changes and activate the plugins, either open a new terminal window or run:
```
bash
source ~/.zshrc
```
