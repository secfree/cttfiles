cttfiles
========

A tool can easily create a lot of files for testing.


Install
------

- Need: Python2.7


Usage
------
```
Usage:
        cttfiles.py [options] directory

    Options:
        -d    create directories, default false, Create directories recursivly, 
                depth of directry is set by argument 'depth'.
        -f    create files, default true
        -h    show help message
        -m    mix mode, default false. Create directories recursivly, then create files in each directory.
              
      Directory
        --depth=DEPTH   directory depth, default 1
        --dnum=DNUM     num of directories, default 10
        --dprefix=DPRE  prefix of directory name
        --dsuffix=DSUF  suffix of directory name

      File
        --exts=EXTS                 file extensions, separated by ','
        --from_dirs=DIRECTORIES     A test file's content is one of file in DIRECTORIES, which is randomly selected.
        --from_files=FILES          A test file's content is one of FILES, which is randomly selected.
        --fprefix=FPRE              prefix of file name
        --fsuffix=FSUF              suffix of file name
        --fnum=FNUM                 num of files, default 10
        --fminsize=FMINSIZE         min size of file when file's content is created randomly. default 1.
        --fmaxsize=FMAXSIZE         max size of file when file's content is created randomly. default 1024.
```

Example
------
```
$ python cttfiles.py -m --depth=2 --dnum=3 --dprefix='dp' --dsuffix='ds' --exts='php,jsp' --from_files="1.jsp,1.php" --fprefix="fp" --fsuffix="fs" --fnum=2 tmp_dir
```
![](https://github.com/secfree/cttfiles/raw/master/cttfiles.jpg)


Copyright (c) 2014 secfree, released under the GPL license
