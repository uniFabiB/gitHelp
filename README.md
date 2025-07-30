# gitHelp

## create new repository
1. `cd` to the local folder
1. initialize local repository
    - `git init`
1. set remote repository using ssh host alias (from ssh config)
    - `git remote add origin gitGithub_unifabib:unifabib/NAMEOFREPO.git`
    - might need to set safe directory
      - `git config --global --add safe.directory /path/to/local/dir`
1. add files either add
    1. manually

       `git add file1.txt file2.script`
    1. all except

       `nano .gitignore`
       
          ```
          #files
          *.o
          *.mod
          #directories
          backup/
          input/
          output/
          temp/
          .git/
          .vscode/
          ```
          `ctrl + o` to write out file
          `ctrl + x` to exit nano
       
       `git add -a`
          
1. commit
    - `git commit -m "initial commit"`
    - `git commit -am "initial commit"`
       which is `git add -A` and `git commit -m`
1. push
    - first push
    
      `git push -u origin master`
    - later just

      `git push`

## clone remote repository using ssh host aliases
- essentially just do everything from `git clone` manually
  1. `cd` to the local folder
  1. initialize local repository
      - `git init`
  1. set remote repository using ssh host alias (from ssh config)
      - `git remote add origin gitGithub_unifabib:unifabib/maxLq.git`
      - might need to set safe directory
        - `git config --global --add safe.directory /path/to/local/dir`
  1. get new changes from remote
      - either pull (=fetch+checkout)
        - `git pull origin master`
        - if remote branch is called main
          - `git pull origin main`    
          - `git branch -m main`
            - this renames the local branch main to match remote branch
            - if not done then always have to `git push -u origin master:main` later
      - or fetch + checkout
        1. update index of remote changes
            - `git fetch`
        1. download and merge remote changes
            - `git checkout master`
  1. do things
  1. commit
     - `git commit -am "commit message"
  1. first push and set upstream for later
     - `git push -u origin main`
- afterwards just
  - `git pull`
  - `git commit -am "commit message"
  - `git push`
     

## helpful commands
- show all branches
    - `git branch -a`
