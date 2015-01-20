#### Using .gitignore to avoid pushing passwords on Github
create .gitignore file<br>
    ```touch .gitignore```

put <FILE_LOCATION> inside .gitignore <br>

move to file location <br>
`ls <FILE_LOCATION>` <br>

remove/untrack file from git<br>
    ```git rm -r --cached <FILE_NAME>```<br>

commit && push<br>
    ```git add.```<br>
    ```git commit -m 'add files to gitignore'```
