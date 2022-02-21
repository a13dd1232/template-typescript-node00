# Git Commands:

## Git Commands List:

git pull

git push


git remote -v

git remote add origin-X

git remote set-url origin 

### Getting Git Default Setting:

git config --global user.name
>>
a13dd1236

git config --global user.email
>>

git remote -v

>>
origin  https://github.com/gitpod-io/template-typescript-node.git (fetch)
origin  https://github.com/gitpod-io/template-typescript-node.git (push)
upstream        https://github.com/microsoft/TypeScript-Node-Starter.git (fetch)
upstream        https://github.com/microsoft/TypeScript-Node-Starter.git (push)


### New Git Default Setting:

** >> 

git config --global user.name
git config --global user.email
git config --global user.email 94798833+a13dd1236@users.noreply.github.com

git remote -v

git remote add upstream-gitpod-io https://github.com/gitpod-io/template-typescript-node.git
git remote add upstream-microsoft https://github.com/microsoft/TypeScript-Node-Starter.git
git remote set-url upstream https://github.com/gitpod-io/template-typescript-node.git

git remote set-url origin https://github.com/a13dd1236/template-typescript-node00.git
git branch -M main
git push -u origin main


#### XxXx XxXx XxXx XxXx XxXx XxXx XxXx XxXx XxXx XxXx 

git remote remove origin 
git remote add origin git@github.com:a13dd1236/template-typescript-node00.git

