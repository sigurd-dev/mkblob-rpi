# mkblob-rpi
Tool to make executables independent from libraries.

Make with makeall_rpi.sh on Raspberry pi camputer. Tested on version 3. 

You might have to tweak the script to make it compile on other distributions.
Also glibc-static is needed to compile. (dnf install glibc-static)
Precompiled binary is included in directory binary_rpi.

mkblob should run on any raspi as it is statically compiled
and includes all files it needs.

With mkblob you can make new library independent executable which you can move
around different Linux distributions. It will gather all the dependecies 
it needs to run and other files your program uses.

Project was originally started to make opencv programs able to run without recompiling/rebuilding/installing.

Example: mkblob /usr/bin/ls -o ls.blob -static

mkblob can be used on not only binaries, but scripts as well, like shell, perl and python and so on.
If you need or want to pass arguments to your (binary) program you should create a script which does this and then run 
this script with mkblob.

There is also an x86_64 and i386 version at: <a href=https://github.com/sigurd-dev/mkblob>https://github.com/sigurd-dev/mkblob</a> 

For more information please visit: <a href=http://www.dagestad.info/mkblob>http://www.dagestad.info/mkblob</a> 

License is for now GPLv3.
