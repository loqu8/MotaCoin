Copyright (c) 2009-2015 Bitcoin Developers
Copyright (c) 2018 MotaCoin Developers
Distributed under the MIT/X11 software license, see the accompanying
file license.txt or http://www.opensource.org/licenses/mit-license.php.
This product includes software developed by the OpenSSL Project for use in
the OpenSSL Toolkit (http://www.openssl.org/).  This product includes
cryptographic software written by Eric Young (eay@cryptsoft.com) and UPnP
software written by Thomas Bernard.

# LINUX (UBUNTU) GUI BUILD NOTES
Tested 2/17/18 on Ubuntu 16.04

## Setup
1. Use `sudo apt-get` as the package manager

## Dependencies
build-essential 4.4.0           `sudo apt-get install build-essential`
boost           1.58.0          `sudo apt-get install libboost-all-dev`
openssl         1.0.2g          `sudo apt-get install libssl-dev`
miniupnpc       1.9.20140610    `sudo apt-get install libminiupnpc-dev`
qrencode        3.4.4           `sudo apt-get install libqrencode-dev`
qt              5.5.1           `sudo apt-get install qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools`
*berkeley-db@4   4.8.30          `sudo apt-get install berkeley-db4`*
libevent        2.0.21          `sudo apt-get install libevent-dev`

or all together:
`sudo apt-get install build-essential libboost-all-dev libssl-dev libminiupnpc-dev libqrencode-dev qt5-default qt5-qmake qtbase5-dev-tools qttools5-dev-tools berkeley-db4 libevent-dev`

## Build MotaCoin-Qt
1. Run `qmake` to create Makefile from MotaCoin-qt.pro
2. Run `make`
