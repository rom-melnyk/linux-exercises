# 02. Files management



## Commands
- `touch`
- `cat`
- `cp`, `mv`, `rm`



## Exercises

### Basic

1. Go to home folder. Create an empty file `1.txt` (using `touch`).
1. Create a folder `/tmp/test/`. Copy the file `1.txt` from home folder to `/tmp/test/`.
   - Use `ls` (or `ll`) to check if file exists at destination.
1. Remove the file `/tmp/test/1.txt` _without leaving home folder._
1. Move `1.txt` from home folder to `tmp/test`.
1. Remove whole folder `/tmp/test/`.
   - Explain why simple `rm` does not work?

### Advanced: hidden files

1. Go to home folder. Create two files: `1.txt` and `.2.txt` (with dor at the beginning).
1. Show the content of the folder via `ls`, `ls -l`.
1. Show the content of the folder via `ll` or via `ls -a`.
1. Learn more about hidden files in Linux.

### Advanced: copy/move folders

1. Check out if `test/` folder exists in `/tmp`. If yes, remove it.
1. Go to home folder. Create a folder `test1/`; go inside and create folder `test2/`.
1. Create a file `~/test1/test2/1.txt`.
1. Go back to home folder.
1. Copy whole `test1/` to `/tmp`.
   Use `cp -R` for this. Explainn why we need extra option for `cp` command.
1. Remove `/tmp/test1`.
1. Move `~/test1/` to `/tmp`.

