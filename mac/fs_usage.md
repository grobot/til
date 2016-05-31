## fs Usage

I have this bug where mystery files are written and never deleted. In
trying to replicate it locally I needed to monitor which processes were
accessing the file system and watching what they did on it.

If you run `sudo fs_usage -f filesys` you will be able to get a running
list of file system accesses. You can then pipe that to `grep` and get
the relevant infomormation
