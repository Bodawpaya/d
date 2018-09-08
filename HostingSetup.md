```bash
apt-get update &&
apt-get install -y language-pack-en-base &&
export LC_ALL=en_US.UTF-8 &&
export LANG=en_US.UTF-8 &&
apt-get install -y software-properties-common &&
apt-get install python-software-properties &&
add-apt-repository ppa:ondrej/php &&
apt-get update && 
apt-get -y upgrade
```

```bash
apt-get -y install unzip zip nginx php7.2 php7.2-mysql php7.2-fpm php7.2-mbstring php7.2-xml php7.2-curl

```
