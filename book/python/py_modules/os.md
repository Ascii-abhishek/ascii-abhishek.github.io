# OS Module

---

| **Command** | **Description**  |
| :---------- | :--------------- |
|```os.access('file', mode)```<br>mode:<br>os.F_OK: found<br>os.R_OK: readable<br>os.W_OK: writable<br>os.X_OK: executable |returns True or false based on mode, 'file' means full path to specific file |
| ```os.chdir('path')``` | change current working directory to path|
| ```os.chmod('file', mode)```<br><br>**mode:**<br>```stat.S_ISUID```: Set user ID on execution<br>```stat.S_ISGID```: Set group ID on execution<br>```stat.S_ENFMT```: Enforced record locking<br>```stat.S_ISVTX```: After execution, save text image<br>```stat.S_IREAD```: Read by owner<br>```stat.S_IWRITE```: Write by owner<br>```stat.S_IEXEC```: Execute  by owner<br>```stat.S_IRWXU```: Read, write, and execute by owner<br>```stat.S_IRUSR```: Read by owner<br>```stat.S_IWUSR```: Write by owner<br>```stat.S_IXUSR```: Execute by owner<br>```stat.S_IRWXG```: Read, write, and execute by group<br>```stat.S_IRGRP```: Read by group<br>```stat.S_IWGRP```: Write by  group<br>```stat.S_IXGRP```: Execute by group<br>```stat.S_IRWXO```: Read, write, and execute by others<br>```stat.S_IROTH```: Read by others<br>```stat.S_IWOTH```: Write by others<br>```stat.S_IXOTH```: Execute by others|Alter the mode of the file, multiple modes can be applied by using 'or' |
|```os.chown('file', uid, gid)```<br>```# os.chown('ab.txt', 100, -1)```| change ownership of file, use -1 to leave it unchanged<br>uid: numeric   user ID<br>gid: numeric group ID |
|```os.chroot(path)``` |change root directory (UNIX) |
|```d_fd = os.dup(fd)``` | create duplicate file descriptor|
| ```os.environ``` | Returns all environment variables. Use os.environ([“HOME”]) like to get specific one. |
|```os.getenv(key, default=none)``` | Return the value of the environment variable key if it exists, or default if it doesn’t.|
| ```os.get_exec_path(env=none) ```| Returns the list of dirs that will be searched for a named executable (like ‘bin’ folder) |
| ```os.getlogin()``` | Returns the name of user logged in. |
| ```os.getpid()``` | Returns current process id|
| ```os.getcwd()``` | returns current working directory |
| ```os.isatty(fd)``` | returns true   if fd is open and is connected to a tty(-like) device, else returns flase |
| ```os.listdir(path)``` | returns list of all items present in path |
| ```os.lseek(fd, pos, how)```<br>how:<br>```os.SEEK_SET``` or 0: pos        relative to the beginning of file<br>```os.SEEK_CUR``` or 1: current position<br>```os.SEEK_END``` or 2: end of the file |Set current position of fd to pos, modified by how |
|```os.major(device)```<br>```os.minor(device)``` |takes a raw device number, and returns the device major, minor number (usually the x.st_dev or x.st_rdev field from x=os.stat('file'))|
| ```os.makedirs(path, mode)```<br>```#os.makedirs('tmp/a/b/c',   0755)``` | like mkdir() (make directory), but here to make c it can also create a and b if not exists |
| ```os.putenv(key, value)``` | Set new environment variables|
| ```os.remove(file)``` | remove a file. if path is given instead of file, OSError will be raised |
| ```os.removedirs(path)``` | remove all directories given in path |
| ```os.rename(src, dst)``` | rename src to   dst, if dst already exists, it raises OSError |
| ```os.rmdir(path)``` | remove a directory |
| ```os.stat(path/file)``` | gives following info about the file or path<br>st_mode: protection bits<br>st_ino: inode number<br>st_dev: device<br>st_nlink: number of hard links<br>st_uid: user id of        owner<br>st_gid: group id of owner<br>st_size: size of file, in bytes<br>   st_atime: time of most recent access<br>st_mtime: time of most recent content modification<br>st_ctime: time of most recent metadata change. |
| ```os.symlink(src, dst)``` | create symbolic link of src folder by name dst. just like desktop shortcut but its for directories not files |
| ```os.tmpfile()``` | temporary file object. deletes itself when no descriptor |
| ```os.uname()``` | Returns system-dependent version information |
| ```os.unsetenv(key)``` | Delete the environment variable named key |
| ```os.umask(mask)``` | Set current numeric umask and return previous umask |
| ```os.walk(top[, topdown=True, onerror=None, followlinks=False)```<br><br>```top:``` Each directory rooted at directory<br>```topdown:``` If topdown is True, or not specified, it scans directories top-down. <br>```onerror:``` This may show  an error to continue with the walk, or may raise an exception to abort the walk.<br>```followlinks:``` This will visit directories that symlinks points to, that is, if set to true.| <br>returns a  generator, Every time the generator is called it will follow each directory   recursively until no further sub-directories are available from the initial   directory that walk was called upon.<br> <br>It Returns:<br>1. Generated  directory path<br>2. Directories in current generated directory<br>3. Files in current generated directory |
| ```os.path.```<br>1. ```join('path1', 'path2')```<br>2. ```basename(path)```<br>3. ```dirname(path)```<br>4. ```split(path)``` <br>5. ```exists('path')```<br>6. ```isdir()```<br>7. ```isfile()```<br>8. ```splitext('path')``` |1. Returns joined paths<br>2. returns base name<br>3. directory name<br>4. ['dir', 'file_name']<br>5. True /False <br>6. True / False<br>7. True /False<br>8. ['path/file_name', 'file_extension']|