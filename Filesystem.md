## [/dev/null](https://prayuja-teli.github.io/Blog/Filesystem)     

/dev/null files are type "c" - character device commonly known /dev/ device file.<br/>
/dev is device in which null is file which is used to eliminating output from terminal.<br/>
/dev/null is null device in unix system. It immediately discards anything written to it.<br/>
/dev/null accept any stream without growing in size.it's size is always zero.

*Character device*-<br/>

A "c" device is one with which the driver communicates by sending and receiving single characters (bytes, octets).Where as driver is software that handles or manages a hardware controller.<br/>

*Null Device* - <br/>

The null device is a device file that discards all data written to it but reports that the write operation succeeded.This device is also sends end of file character to any process reading data from it.<br/>

*Device Filesystem* -<br/>

The /dev/ device is a mountpoint for the devfs (Device Filesystem) pseudo-filesystem.<br/>
devfs is a device manager in the form of a filesystem that displays each device as files. <br/>
This pseudo/virtual filesystem is not on the hard-drive.rather,it is in memory.<br/>
The null device is typically used for disposing of unwanted output streams of a process.<br/>

*File Descriptor* -<br/>

A file descriptor is a number that uniquely identifies an open file in a computer's operating system.<br/>
There are three file descriptor in dev directory stderr , stdin , stdout and null is filetype where this file descriptor directs.<br/>
These are file descriptor are represented in numbers as - <br/>
stdin (standard input, file descriptor 0)<br/>
stdout (standard output, file descriptor 1)<br/>
stderr (standard error, file descriptor 2).<br/>







#### Feel free to share feedback
