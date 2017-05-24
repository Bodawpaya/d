# node

```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
nvm install node
npm i bower vtop yarn webpack  -g
```

# git
```
sudo apt-get install git
git config --global "$email"
git config --global user.name "$username"
```

# Github
```
cd && cd .ssh
ssh-keygen -t rsa -b 4096 -C "$email"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/github_nayzawoo
cat github_nayzawoo.pub | xclip -selection clipboard

# Paste ssh-key on github ssh setting
# > https://github.com/settings/ssh

# Testing your SSH connection
ssh -T git@github.com
 ```

# rb
```
sudo apt install rbenv
```

# php
```
sudo apt install php-curl php-gd php-json php-mbstring \
php-mcrypt php-common php-mysql php-xml php-mongodb php-memcached zip unzip \
php-dev \
apache2 libapache2-mod-php \
sudo a2enmod rewrite
/etc/init.d/apache2 restart
```

# vhost
```
cd /usr/local/bin
sudo wget -O virtualhost https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost.sh
sudo chmod +x virtualhost
```

# composer

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```

# vi
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:neovim-ppa/stable
sudo apt-get update
sudo apt-get install neovim
sudo apt-get install vim-gnome 
```

# Ubuntu
```
sudo add-apt-repository ppa:noobslab/indicators
sudo add-apt-repository ppa:indicator-multiload/stable-daily
sudo add-apt-repository ppa:noobslab/themes
sudo add-apt-repository ppa:noobslab/icons
sudo apt-add-repository ppa:numix/ppa
sudo add-apt-repository ppa:flexiondotorg/albert


sudo apt update

sudo apt-get install numix-icon-theme numix-icon-theme-circle \
unity-tweak-tool gnome-tweak-tool synapse copyq indicator-multiload  arc-theme docky
```








