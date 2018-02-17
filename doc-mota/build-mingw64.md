Copyright (c) 2009-2015 Bitcoin Developers
Copyright (c) 2018 MotaCoin Developers
Distributed under the MIT/X11 software license, see the accompanying
file license.txt or http://www.opensource.org/licenses/mit-license.php.
This product includes software developed by the OpenSSL Project for use in
the OpenSSL Toolkit (http://www.openssl.org/).  This product includes
cryptographic software written by Eric Young (eay@cryptsoft.com) and UPnP
software written by Thomas Bernard.

# WINDOWS (MINGW64) GUI BUILD NOTES
Tested 2/17/18 on Windows Server 2012

## Setup
1. Install 64-bit MSYS2 from http://www.msys2.org/
2. Use `pacman` as the package manager
3. Start MINGW64 shell by clicking on the "Mingw-w64 64 bit" button

## Dependencies
git             2.16.1          `pacman -S git`
toolchain                       `pacman -S base-devel mingw-w64-x86_64-cmake mingw-w64-x86_64-toolchain`
boost           1.66.0          `pacman -S mingw-w64-x86_64-boost`
openssl         1.0.2m          `pacman -S openssl`
miniupnpc       2.0.20180203    `pacman -S mingw-w64-x86_64-miniupnpc`
qrencode        3.4.4           `pacman -S mingw-w64-x86_64-qrencode`
qt              5.10.1          `pacman -S mingw-w64-x86_64-qt5-static`
libevent        2.1.8           `pacman -S libevent`

or all together:

`pacman -S git mingw-w64-x86_64-toolchain mingw-w64-x86_64-boost openssl mingw-w64-x86_64-miniupnpc mingw-w64-x86_64-qrencode mingw-w64-x86_64-qt5-static libevent`

### Berkeley DB4
This must be manually installed as the current version is 5.3.28. See https://bitcointalk.org/index.php?topic=45507.0 for discussion. Download the DB4 source code from http://www.oracle.com/technetwork/database/database-technologies/berkeleydb/downloads/index-082944.html.

`../dist/configure --disable-replication --enable-mingw --enable-cxx --prefix=/usr/local`

db.h in build_unix/
@ Line 113 Replace `typedef pthread_t db_threadid_t;` with `typedef u_int32_t db_threadid_t;`

Then `make install`. 

## Build MotaCoin-Qt.exe
1. Run `qmake` to create Makefile from MotaCoin-qt.pro
2. Run `make`
