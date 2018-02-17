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
boost           1.66.0          `sudo apt-get install boost`
openssl         1.0.2n          `sudo apt-get install openssl`
miniupnpc       2.0.20180203    `sudo apt-get install miniupnpc`
qrencode        4.0.0           `sudo apt-get install qrencode`
qt              5.10.1          `sudo apt-get install qt5`
berkeley-db@4   4.8.30          `sudo apt-get install berkeley-db4`
libevent        2.1.8           `sudo apt-get install libevent`

## Build MotaCoin-Qt.exe
1. Run `qmake` to create Makefile from MotaCoin-qt.pro
2. Run `make`
