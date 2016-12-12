# Simple Git Deployment

Easy as 1, 2, 3

## 1

Create a bare git repo somewhere private

    cd /var/www/example.com/private
    git init --bare example.git

## 2

Copy `post-receive` into the `hooks` folder. Make any changes as needed.

> Don't forget to make it executable (`chmod a+x post-receive`)
 
## 3

On your local repository, add the remote, then push.

    git remote add production user@myserver:/var/www/example.com/private/example.git
    git push production master
