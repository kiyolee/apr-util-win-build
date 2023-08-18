# apr-util-win-build

Apache apr-util Windows build with Visual Studio.

This version is apr-util-1.6.3.

To build, simply open the required solution file, and
you know how to use Visual Studio, right?
(or perhaps this is the wrong place for you.)

Depends on:
* libiconv-win-build  
* zlib-win-build  
* openssl3-win-build  
* expat-win-build  
* apr-win-build  

There are hard references assuming all these sit next to apr-util-win-build.

Basically, in a command prompt:

> \> cd {somewhere}\\  
> \> git clone https://github.com/kiyolee/libiconv-win-build.git  
> \> git clone https://github.com/kiyolee/zlib-win-build.git  
> \> git clone https://github.com/kiyolee/openssl3-win-build.git  
> \> git clone https://github.com/kiyolee/expat-win-build.git  
> \> git clone https://github.com/kiyolee/apr-win-build.git  
> \> git clone https://github.com/kiyolee/apr-util-win-build.git  

Build all these dependencies in the suggested order as shown above and finally apr-util, with the same corresponding Visual Studio solution of course.

### Notes:

* dbm odbc and crypto openssl drivers are embedded. Corresponding driver DLLs are neither built nor needed by design.
* LDAP functionality is not available currently.
