# Add SSH keys

	cd && cd .ssh
	ssh-keygen -t rsa -b 4096 -C "$email"
	eval "$(ssh-agent -s)"
	ssh-add ~/.ssh/github_nayzawoo
	cat github_nayzawoo.pub | xclip -selection clipboard

	# Paste ssh-key on github ssh setting
	# > https://github.com/settings/ssh

	# Testing your SSH connection
	ssh -T git@github.com

## run agent


```
eval "$(ssh-agent -s)"
vim ~/.ssh/config

Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

## Cache Auth

```
git config --global credential.helper store
```
