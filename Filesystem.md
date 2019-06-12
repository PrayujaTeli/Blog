## [/dev/null](https://prayuja-teli.github.io/Blog/Filesystem)     

> ## Definition<br/>

#### /dev/null 

/dev/null is the most commonly known /dev/ device file.<br/>
/dev/null files are type c - character device.<br/>

*Character device*-


/dev is directory,null is file in /dev directory which is used to get output from or to redirect output to this file,mainly this file is used to eliminating output from terminal.<br/>
/dev/null is null device in unix system. It immediately discards anything written to it.<br/>
/dev/null accept any stream without growing in size.it's size is always zero.

*Null Device* - 
The null device is a device file that discards all data written to it but reports that the write operation succeeded.This device is also sends End of file character to any process reading data from it.<br/>

*Device Filesystem* -
The "/dev/" directory is a mountpoint for the devfs (Device Filesystem) pseudo-filesystem.<br/>
devfs is a device manager in the form of a filesystem that displays each device as files. <br/>
This pseudo/virtual filesystem is not on the hard-drive. Rather, it is in memory.<br/>
The null device is typically used for disposing of unwanted output streams of a process.<br/>

*File Descriptor* -
A file descriptor is a number that uniquely identifies an open file in a computer's operating system.<br/>
There are three file descriptor in dev directory stderr , stdin , stdout and null is filetype where this file descriptor directs.<br/>
These are file descriptor shown in number pattern stdin (standard input, file descriptor 0), stdout (standard output, file descriptor 1) and stderr (standard error, file descriptor 2).<br/>







