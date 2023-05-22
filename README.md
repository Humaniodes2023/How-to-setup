
# How to setup a git enviroment 
1.- Download git from [Git-downloads](https://git-scm.com/downloads)

2.- Create a github account on [Github-Create account](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)

3.- On git bash or normal cli link your Git with github.

```bash 
git config --global user.name “[firstname lastname]”
git config --global user.email “[valid-email]”
```
4.- Clone this proyect by copying and changing the next command.
```bash 
git clone [repository link]
```
---


# Creating and moving between branches

1.- We need to fetch the changes on the branches by doing the next command.

```bash 
git fetch
```

2.- The we have to change branches, wheather we are on main or any other created with the next command.

```bash 
git checkout <branch name>
```

2.1.- To check current branches use this command.
```bash 
git branch
```
2.1.2.- The branches will look like (asterisk *) for the one you are in 
```bash 
$ * main 
   <branch name>
   <branch name>
```
3.- To create a new branch locally and move to it type this next command
```bash 
git checkout -b <branch name>
```

4.- To upload your local branch to github 

```bash
git push origin <branch name>
```

5.- To link your local branch with a branch on github being on your branch
```bash 
git branch -u upstream/<branch name on github>
```

5.1.- To link your local branch with a branch on github while not being on your branch
```branch
git branch -u upstream/<branch name on github> <branch name locally>
```

# Working on a proyect 
## Get on date files 
### In case there are multiple branches
First we need to download all changes, if the proyect has branches you need to type the next commands:
```bash
git fetch
```
Then you have to pull the changes to your local enviroment with this command:
```bash
git pull
```
And you are up to date!

### In case there are no branches outside main
In this case you only need to pull the changes as showned before. Just like this:
```bash
git pull
```

## Once it is on date with all changes on github files

If you have any changes uncommited you have to stage them to check which files are different or which ones are new use the next command.

```bash 
git status
```

1.- To Stage any changes to commit you can use this commands

```bash
git add <name of the file>
```
or you can stage all the changes with
```bash
git add .
```

1.1.- To remove any change staged you can use this command

```bash
git rm <name of the file>
```

2.- To commit your staged files use this commands

It will open your default message editor to give a small description of your commit
```bash
git commit 
```
In case you want to type your message directly on your commit.
```bash
git commit -m "HERE GOES YOUR DESCRIPTION"
```
3.- To push your commits to github use this command.

```bash
git push
```
# Gitignore
To make git ignore files or folders that have sensitive information like passwords or have information that is not important.

To add files to ignore add them to the file named ".gitignore" add them like this:
```gitignore
# For folders
folder/
# For files
file.txt
```

# Recap 
- If you are going to start a proyect you have to clone it 
- If you have the proyect and want to do some changes:
   - Fetch branches
   - Pull changes
- If you are up to date, use "git status" to check if you have unstaged changes
- Use the ".gitignore" file to ignore files or folders that are not necessary or that have sensitive information. (Most hacks occur because the sensite information is not ignored and people see your credentials on a Github repository)

## Authors
In case you have any doubt dont hesitate on contacting me 

My Github profile
- [@AlanGallegosEsp](https://github.com/AlanGallegosEsp)

- lunaespindola04@gmail.com