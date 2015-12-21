### Vim reminders
#####Use vi-mode in Bash
```set -o vi```
<br>
#####close all windows but the one you are in
```<Ctrl>W``` then ```o```
<br><br>

#####if vim is complaining about .swp, do this in your /.vimrc.local <br>
```set backupdir=/var/tmp,/tmp```<br>
```set directory=/var/tmp,/tmp```
<br><br>
Now you can just nuke the swap files in one swoop when you are annoyed:<br>
```rm -rf /var/tmp/*.swp```
<br><br>
#####Vim didn't compile with the language support you want?
Check via `vim --version` for `+python` if supported, `-python` if not supported <br><br>
In the case that it's not supported, you have to reinstall with the language flag on. <br>
`brew uninstall macvim`<br>
`brew install macvim --with-python`

### Bash reminders
##### finding processes and killing them with:
`ps aux | grep <keyword>` to get PID number<br>
`kill -9 <pid>`


##### Using .gitignore to avoid pushing passwords on Github
create .gitignore file<br>
    `touch .gitignore`

put <FILE_LOCATION> inside .gitignore <br>

move to file location <br>
`cd <FILE_LOCATION>` <br>

remove/untrack file from git<br>
    `git rm -r --cached <FILE_NAME>`<br>

commit && push<br>
    `git add.`<br>
    `git commit -m 'add files to gitignore'`

#####how to change shell (bash/zsh/etc)<br>
`chsh -s <SHELL_PATH>`
where `SHELL_PATH` is usually `/bin/bash` or `/bin/zsh`

#####how to create a symlink<br>
```bash
  cd /
  mkdir /A; mkdir /B
  touch /A/X; touch /B/Y
  ln -s /B/Y /A/New
 ```
 `A/New` is now a symlinked to `/B/Y`
