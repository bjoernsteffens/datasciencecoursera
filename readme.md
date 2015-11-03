## Cheat sheet for setting up github on Apple

http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1

## Cheatsheet for managing Github

http://www.dataschool.io/git-quick-reference-for-beginners/

http://ndpsoftware.com/git-cheatsheet.html#loc=local_repo;

## Github Workflow - here is where the coin drops ...

1. Fork a project. The project you are forking is referred to as the upstream repo
2. Make changes to your project and apply the changes to your copy/fork at your Github account
3. Create a pull request if you want to contribute to the original project you forked. This will send a notification to the owner of the original repo to review and accept/reject your proposed changes.

## Something about different workflows

http://blog.scottlowe.org/2015/01/27/using-fork-branch-git-workflow/

## My Credentials

  uid / pwd xxx / yyy

## Set up Git

https://help.github.com/articles/set-up-git/

git config --global user.name "Bjoern W. Steffens"

git config --global user.email "bjoern.steffens1@gmail.com"

https://help.github.com/articles/generating-ssh-keys/

cd

ls -al ~/.ssh

Look for

id_dsa.pub

id_ecdsa.pub

id_ed25519.pub

id_rsa.pub

If they don't exist create them

ssh-keygen -t rsa -b 4096 -C "bjoern.steffens1@gmail.com"

passphrase: your_very_long_passphrase

Accept to save to

/Users/bjoernsteffens/.ssh/id_rsa.pub

Add the keys to the ssh agent

eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_rsa

Add the SSH keys to your account

Copy it to the clipboard

pbcopy < ~/.ssh/id_rsa.pub

Add it to the GitHub account settings

![alt text](https://github.com/bjoernsteffens/datasciencecoursera/blob/master/ssh_keys.png "Adding your ssh keys to your Github accunt")

## Test the connection

ssh -vT git@github.com

ssh -T git@github.com

Hi bjoernsteffens! You've successfully authenticated, but GitHub does not provide shell access.
Bjoern-Private-MacBook:.ssh bjoernsteffens$

## Start working with GitHub

Create the repo on GitHub

Open a command line

Cd to where ever you want to work on your code

Clone the repo

mkdir nodejs_git

git clone git@github.com:bjoernsteffens/nodejs.git

Work on your code and push it back to the repo

vi your_file1

vi your_file2

git add your_file1

git add your_file2

git commit -m "Bjoern is committing his first changes"

git push origin master

## Process - Change and push files when done

git add $the_file_that_changed

git commit -m "Bjoern is committing more changes"

git push origin master
