# Basic Shell/UNIX Commands

Keep in mind that not all of these commands are native to UNIX itself, and you may not encounter them on every UNIX system. Still, they can generally be used in the same way—by typing the command and pressing return. On non-Solaris systems, some commands may behave differently [see SunOS differences for details](https://mally.stanford.edu/~sr/computing/sunos-diffs.html)

If you make a typo, the quickest fix is to press CTRL‑u to clear the entire line. Alternatively, you can edit the command directly [see the More UNIX guide for tips](https://mally.stanford.edu/~sr/computing/more-unix.html#com)

Also remember: **UNIX is case-sensitive**.

# Bash Command Reference

## Files
- `ls` — list files in the current directory  
- `ls -l` — long format listing (size, owner, permissions, last modified)  
- `ls -a` — show all files, including hidden ones (dot-prefixed)  
- `more filename` — view file contents one screen at a time (`space` to continue, `q` to quit, `/pattern` to search)  
- `nano filename` or `vim filename` — edit or create a file (alternative to `emacs`)  
- `mv file1 file2` — rename or move a file  
- `cp file1 file2` — copy a file  
- `rm filename` — delete a file (use `rm -i` for confirmation)  
- `diff file1 file2` — compare two files line by line  
- `wc filename` — count lines, words, and characters in a file  
- `chmod options filename` — change file permissions (e.g., `chmod o+r file` makes it readable by others)

## File Compression
- `gzip filename` — compress a file (`.gz` extension added)  
- `gunzip filename` — decompress a gzipped file  
- `zcat filename` — view contents of a gzipped file without decompressing  

## Printing
- `lpr filename` — print a file (`-P printername` to specify printer)  
- `lpq` — check printer queue  
- `lprm jobnumber` — remove a job from the queue  

## Directories
- `mkdir dirname` — create a new directory  
- `cd dirname` — change directory (`cd ..` moves up one level, `cd` returns to home)  
- `pwd` — show current directory path  

## Finding Files
- `find . -name "filename"` — search for files recursively from current directory  
- `grep string file(s)` — search for text patterns in files (`egrep` and `fgrep` provide variations)  

## User Information
- `w` — show who is logged in and what they’re doing  
- `who` — list logged-in users and their locations  
- `finger username` — display user info (last login, mail, .plan file)  
- `last -1 username` — show last login/logout for a user  
- `talk username` — start a live text conversation  
- `write username` — send one-line messages  

## Self Information
- `whoami` — display your username  
- `passwd` — change your password  
- `ps -u username` — list your processes (with IDs)  
- `kill PID` — terminate a process (`kill -9 PID` forces termination)  
- `quota -v` — show disk quota and usage  
- `du filename` — show disk usage (`du -s` for summary)  
- `last username` — list your login history  

## Remote Connections
- `ssh hostname` — connect to a remote host securely  
- `scp file host:/path` — copy files to/from a remote host  
- `ftp hostname` — transfer files (use `get`, `put`, `mget`, `mput`; note: not secure)  
- `lynx` — text-based web browser  

## Miscellaneous Tools
- `date` — show current date and time  
- `cal` — display calendar (`cal 10 1995` for October 1995, `cal 1995` for full year)  
- `man command` — view manual page for a command  

