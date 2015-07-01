#### finding processes and killing them with:
```ps aux | grep <keyword>``` to get PID number<br>
```kill -9 <pid>```

#### if vim is complaining about .swp, do this in your /.vimrc.local
```set backupdir=/var/tmp,/tmp```<br>
```set directory=/var/tmp,/tmp```
##### Now you can just nuke the swap files in one swoop when you are annoyed:
```rm -rf /var/tmp/*.swp```

#### Using .gitignore to avoid pushing passwords on Github
create .gitignore file<br>
    ```touch .gitignore```

put <FILE_LOCATION> inside .gitignore <br>

move to file location <br>
`cd <FILE_LOCATION>` <br>

remove/untrack file from git<br>
    ```git rm -r --cached <FILE_NAME>```<br>

commit && push<br>
    ```git add.```<br>
    ```git commit -m 'add files to gitignore'```
