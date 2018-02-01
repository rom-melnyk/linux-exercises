# 01. Folders tree



## Commands
- `pwd`, `cd`
- `mkdir`, `rm -rf`



## Exercises

### Walking down the directory tree

1. Where are you? What's the path to current folder?
   - Check this out in terminal prompt and via the command.
1. Go to root and go back.
   - Use `cd -` to go back. Check out how it behaves by repetitive use.
1. What is your user's home folder?  
   Go to `/opt` and get back to home folder.
   - Try two ways: via absolute/relative path and via `~`.
1. Absolute and relative path:
   - Go to your home folder; go to `/tmp`; get back using _relative_ path.
   - Where will you appear after `cd ~/../../tmp`? Explain the answer.

### Creating and removing folders

1. Go to `/tmp` and create a folder `test` there.
1. Remove that folder. What's the difference between `rm something` and `rm -r something`?
1. Go to home folder. Create a folder `test` in `/tmp` _without leaving current folder!_
1. Remove `/tmp/test` _without leaving current (home) folder._ Use relative path.

**Note:** Use `ls -al` (alias `ll` in Ubuntu) to check if the folder exists. Mind that this command accepts path if you want to list the content of some distant folder.


