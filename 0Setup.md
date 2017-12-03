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

# Web
```
sudo apt install curl php-curl php-gd php-json php-mbstring \
php-mcrypt php-common php-mysql php-xml php-mongodb php-memcached zip unzip \
php-dev php-bcmath \
memcached \
apache2 libapache2-mod-php or libapache2-mod-php7.0 
sudo a2enmod rewrite

/etc/init.d/apache2 restart


sudo apt install beanstalkd
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
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '669656bab3166a7aff8a7506b8cb2d1c292f042046c5a994c43155c0be6190fa0355160742ab2e1c88d40d5be660b410') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
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
indicator-multiload  arc-theme docky xdman \
flatabulous-theme activity-log-manager \
python-dev python3-dev \
keepassx vlc
```



## Tweak

[zeitgeist-fts](https://askubuntu.com/questions/339212/zeitgeist-fts-always-using-a-lot-of-memory)



