# apr-util-win-build

Apache apr-util Windows build with Visual Studio.

This version is apr-util-1.6.4.

To build, simply open the required solution file, and
you know how to use Visual Studio, right?
(or perhaps this is the wrong place for you.)

Depends on:
* libiconv-win-build  
* zlib-win-build  
* openssl-win-build:main (openssl 4 for VS2015 or later)  
* openssl-win-build:openssl-3.6 (openssl 3.6 for VS2013)  
* openssl1_1-win-build (openssl 1.1 for VS2010)  
* expat-win-build  
* apr-win-build  

There are hard references assuming all these sit next to apr-util-win-build.

Basically, in a command prompt:

> \> cd {somewhere}\\  
> \> git clone https://github.com/kiyolee/libiconv-win-build.git  
> \> git clone https://github.com/kiyolee/zlib-win-build.git  
> \> git clone https://github.com/kiyolee/openssl-win-build.git (openssl 4 for VS2015 or later)  
> \> git clone -b openssl-3.6 https://github.com/kiyolee/openssl-win-build.git openssl3-win-build (openssl 3.6 for VS2013)  
> \> git clone https://github.com/kiyolee/openssl1_1-win-build.git (openssl 1.1 for VS2010)  
> \> git clone https://github.com/kiyolee/expat-win-build.git  
> \> git clone https://github.com/kiyolee/apr-win-build.git  
> \> git clone https://github.com/kiyolee/apr-util-win-build.git  

Build all these dependencies in the suggested order as shown above and finally apr-util, with the same corresponding Visual Studio solution of course.

### Notes:

* dbm odbc and crypto openssl drivers are embedded. Corresponding driver DLLs are neither built nor needed by design.
* LDAP functionality is not available currently.
