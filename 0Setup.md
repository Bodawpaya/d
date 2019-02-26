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
sudo apt install redis-server
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
php -r "if (hash_file('sha384', 'composer-setup.php') === '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
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


## Cert

```
sudo apt-get install software-properties-common
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update
sudo apt-get install certbot python-certbot-nginx 
```


