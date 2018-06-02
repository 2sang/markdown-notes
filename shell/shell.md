#### Useful history commands - [Thegeekdiary](https://www.thegeekdiary.com/unix-linux-examples-of-bash-history-command-you-may-have-never-used/)
Repeat last command starting with some character:
```bash
$ !uname
uname -a
$ !git
git push origin master
```
Repeat last command that contains some character
```bash
$ echo "I am legend"
I am legend
$ !?legend
$ echo "I am legend"
I am legend
```

#### If you use different shell other than bash:
If you feel better working with default shell other than bash, just make sure you make them work independently.
for example, if you sourcing each other by calling '. ~/.bashrc', or  'source ~/.bashrc' in ~/.zshrc, or vice versa,
not only they **aren't compatible**, but it only makes code dirty and hard to maintain.


