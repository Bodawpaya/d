## Init
```
apt install software-properties-common python-software-properties
```

## Repos
```
sudo add-apt-repository ppa:neovim-ppa/stable
sudo add-apt-repository ppa:noobslab/indicators
sudo add-apt-repository ppa:indicator-multiload/stable-daily
sudo add-apt-repository ppa:noobslab/apps
sudo add-apt-repository ppa:noobslab/themes
sudo add-apt-repository ppa:noobslab/icons
sudo apt update
```

# node

```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
nvm install node
npm i bower vtop yarn webpack npm-check-updates  -g
```

# Version Control
```
sudo apt-get install subversion git
git config --global "$email"
git config --global user.name "$username"
git config credential.helper 'cache --timeout=10800'
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

# SSH
https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands

# Web
```
sudo apt install mysql-server
sudo mysql_secure_installation
sudo apt install curl php-curl php-gd php-imagick php-json php-mbstring \
php-common php-mysql php-xml php-mongodb php-memcached zip unzip \
php-dev php-bcmath \
memcached \
apache2 libapache2-mod-php or libapache2-mod-php7.0 
sudo a2enmod rewrite

/etc/init.d/apache2 restart


sudo apt install beanstalkd
sudo apt-get install supervisor

```

# Nginx

```
https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-in-ubuntu-16-04
https://www.digitalocean.com/community/tutorials/how-to-install-laravel-with-an-nginx-web-server-on-ubuntu-14-04
```

# vhost
```
cd /usr/local/bin
sudo wget -O virtualhost https://raw.githubusercontent.com/RoverWire/virtualhost/master/virtualhost.sh
sudo chmod +x virtualhost
```

# composer

```
cd /tmp
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```

# vi
```
sudo apt-get install neovim vim-gnome 
```

# Ubuntu
```
sudo apt-add-repository ppa:numix/ppa

sudo apt-get install build-essential numix-icon-theme numix-icon-theme-circle \
unity-tweak-tool gnome-tweak-tool synapse copyq \
indicator-multiload  arc-theme docky activity-log-manager \
python-dev python3-dev \
keepassx vlc
```

```
sudo add-apt-repository ppa:system76/pop
sudo apt update
sudo apt install pop-theme
```


## Tweak

[zeitgeist-fts](https://askubuntu.com/questions/339212/zeitgeist-fts-always-using-a-lot-of-memory)



