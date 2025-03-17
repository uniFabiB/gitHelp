# gitHelp

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
      - (potentially `git pull` in future if default branch set)
    - or fetch + checkout
      1. update index of remote changes
          - `git fetch`
      1. download and merge remote changes
          - `git checkout master`  


## helpful commands
- show all branches
    - `git branch -a`
