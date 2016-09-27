# Add SSH keys

	cd && cd .ssh
	# Creates a new ssh key && provide your_ssh_key_name
	ssh-keygen -t rsa -b 4096 -C "nayyzawoo.me@mail.com"
	
	# start the ssh-agent in the background
	eval "$(ssh-agent -s)"
	ssh-add ~/.ssh/your_ssh_key_name
	cat your_ssh_key_name.pub | xclip -selection clipboard

	# Paste ssh-key on github ssh setting
	# > https://github.com/settings/ssh

	# Testing your SSH connection
	ssh -T git@github.com
