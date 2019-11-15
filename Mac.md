brew install watchman

### Essential

```bash
# brew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# window manager
brew cask install shiftit
brew install wget
brew install thefuck
brew cask install iterm2
brew install git-extras
brew install git bash-completion
brew install bash-git-prompt
## .bash_profile
## export CLICOLOR=1
brew install lazygit

brew cask install macpass
brew cask install vlc
brew install htop
brew cask install gimp
# composer
# https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos
export PATH=~/.composer/vendor/bin:$PATH
brew install php
composer global require laravel/valet
# go
brew install golang
export GOPATH=$HOME/go-workspace # don't forget to change your path correctly!
export GOROOT=/usr/local/opt/go/libexec
export PATH=$PATH:$GOPATH/bin
export PATH=$PATH:$GOROOT/bin

brew install vim
brew install mysql
brew services start mysql

#node
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash

#php-ext

brew install pkg-config
brew tap josegonzalez/php
brew install imagemagick
pecl install imagick
sudo pecl install grpc

```
# tap to click
sys pref > trackpad 


```

### Switch Cap->Esc

- `System Preferences` -> `Keyboard` -> `Keyboard Tab` -> `Modifier Keys` -> Change

### Use the Tab Key to Switch Between Dialog Buttons in Mac OS X

- `Preferences` > `Keyboards` > `Shortcuts Tab` 
  - `Full Keyboard Access` to `"All controls"`


### Apps

phpstorm,androidstudio,subl,code,libreoffice,gimp,chrome,firefox,neovim,gitkraken
bandwidth+, skype,dbraver

### Faster Dock

```bash
defaults write com.apple.dock autohide-time-modifier -float 0.15;killall Dock
defaults write com.apple.dock autohide-delay -float 0; killall Dock

# reverse
defaults delete com.apple.dock autohide-time-modifier;killall Dock
defaults delete com.apple.dock autohide-delay; killall Dock
```

### faster key repeate

```
#disable shits
defaults write -g ApplePressAndHoldEnabled -bool false
```
