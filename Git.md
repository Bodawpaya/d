# Update Git

	sudo add-apt-repository ppa:git-core/ppa -y
	sudo apt-get update
	sudo apt-get install git -y
	git --version

# Change the author and committer name and e-mail of multiple commits in Git

```bash
#!/bin/sh

git filter-branch --env-filter '
OLD_EMAIL="old@email.com"
CORRECT_NAME="My Name"
CORRECT_EMAIL="myname@example.com"
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --
```


## Download single directory from a Github Repository

Eg: 
Repository URL: **https://github.com/lodash/lodash** 
Folder: **/docs**

	svn checkout https://github.com/lodash/lodash/trunk/docs


## Recover Deleted File From Commit

	git rev-list -n 1 HEAD -- <file_path>
	git checkout <deleting_commit>^ -- <file_path>

## 	Git clone just the latest revision

	git clone --depth=1 <remote_repo_url>