## Text processing:

### grep 
seraches for string in group of files.

## Sed 's/to-be-replaced/new-word' filename
- it is used for searching, inserting etc..
### sed 's/*//' /etc/passwd
prints all the content
- ex: root:x:0:0:root:/root:/bin/bash
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
### sed 's/:.*//' /etc/passwd
- prints the content till :
ex:root
bin
daemon
- same command in other way
###  sed 's/\([^:]*\).*/\1/' /etc/passwd
- prints the content till :
o/p :root
bin
daemon

-here we are dividing and storing two diffenet groups
sed 's/\    ([^:]*\)    \   (.*\)   /\2/' /etc/passwd
            group1          group2
-group1: stores till the : from whole output
-group2: stores rest starting from :

###  sed 's/\([^:]*\).*/\1/' /etc/passwd
- prints the content till :
ex o/p :root
bin
daemon

###  sed 's/\([^:]*\)\(.*\)/\2/' /etc/passwd
- prints rest of the content.
o/p:
:x:0:0:root:/root:/bin/bash
:x:1:1:bin:/bin:/sbin/nologin
:x:2:2:daemon:/sbin:/sbin/nologin

### sed '/enetr text where we need to insert/i----' file_name
![screenshot](https://github.com/SrinivasEsapalli/Git/blob/main/text_proccessing_cmd/screenshot/sed_insertion.jpg)






