## Cheat sheet for setting up github on Apple

  http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1

## My Credentials

  uid / pwd xxx / yyy

## Set it up

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