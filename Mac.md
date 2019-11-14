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
brew install zsh zsh-completions
chsh -s /bin/zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
brew install git-extras
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
# https://golang.org/dl/

#node
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
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
bandwidth+,

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
