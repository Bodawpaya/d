# [Installation(16.10)](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04)

# Node, NPM
- https://github.com/creationix/nvm

# Customize System Notification Timeout

    sudo add-apt-repository ppa:leolik/leolik
    sudo apt-get update
    sudo apt-get install libnotify-bin 
    sudo apt-get install notify-osd

Restart the daemon
    
    pkill notify-osd

Install NotifyOSD Configuration(GUI)

    sudo add-apt-repository ppa:nilarimogard/webupd8
    sudo apt-get update
    sudo apt-get install notifyosdconfig

