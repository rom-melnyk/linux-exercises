# Linux exercises: file permissions

## Create a private folder

### Prerequisites and useful commands

1. Make sure there are 2+ different users in the system.
   An easy way to create a user is *Settings* > *User* then follow "Add new user" routine.
   - Each user has their own home folder (referenced as `~`) which is `/home/USER-NAME/`.
     The command `cd ~` or the path `~/test.txt` refer to different places being called by different users.
1. The command `su USER-NAME` changes the user. The command prompt (`markiian@my-comp:~/test $`) looks different for different users.
   After performing `su USER-NAME` you are able to run commands as `USER-NAME`.
   Type `exit` to leave the `USER-NAME`'s session and get back to your main account (`markiian@...`).
1. The command `whoami` prints the name of current user.
   It's like `pwd` but for users.
1. File/folder permissions which is shown by `ls -al` or by `ll`:
   ```
   _ rwx rwx rwx
   :  :   :   :
   :  :   :   :....... Others
   :  :   :........... Group
   :  :............... User (owner)
   :.................. a type marker ("d" for a folder, nothing means a file)

   Where RWX stand for Read, Write and eXecute respectively.
   ```
1. Use `chmod` command to change file/folder permissions:
   `chmod u+x file.sh` sets the eXecutable flag (think "makes file an executable") for a user;
   `chmod u-x file.sh` clears the eXecutable flag for user (so file is not executable anymore);
   `chmod g+r file.sh` allows Group members to read this file;
   `chmod o-w file.sh` disallows Others (neither a user, nor a group member) to read the file;
   `chmod a+r file.sh` sets the Read flag for all (User, Group and Others).
1. A "superuser" called `root` can do anything with any file/folder in the system. Read/Write permission limitations don't work against superuser.
   However, the superuser respects the eXecutable permissions.
   Perform `sudo su` to start superuser session and `exit` to leave it.
   You can also do `su SOME-COMMAND` to perform that command as a superuser (so called "temporary `su` session").
   Mind that not every user can do it but only members of the `sudoers` group.



## Create and test a private folder

1. As user `markiian`, create a folder `secret` in your home folder.
1. Set following permissions to that folder: `d rwx ___ ___`.
   This makes folder inaccessible for anyone but a user. A folder *must have* eXecutable flag set otherwise you cannot `cd` into it!
1. The folder with permissions `d rwx r_x r_x` is a read-only for anyone but owner.
   No one else can write anything into that folder; no one else can delete anything from that folder.

### How to test

After creating a folder and setting appropriate permissions, perform `su ANOTHER-USER` and try to `cd secret`.
Type `exit` to leave `ANOTHER-USER`'s session back to `markiian`.



## Create a read-only file

It's needed sometimes a file to be read-only. In order to do that remove the Write permissions by doing `chmod a-w path/to/file`.
You can leave the Write permissions for user so there is less annoying if you need to change it.
