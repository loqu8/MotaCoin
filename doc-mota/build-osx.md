Copyright (c) 2009-2015 Bitcoin Developers
Copyright (c) 2018 MotaCoin Developers
Distributed under the MIT/X11 software license, see the accompanying
file license.txt or http://www.opensource.org/licenses/mit-license.php.
This product includes software developed by the OpenSSL Project for use in
the OpenSSL Toolkit (http://www.openssl.org/).  This product includes
cryptographic software written by Eric Young (eay@cryptsoft.com) and UPnP
software written by Thomas Bernard.

# OSX GUI BUILD NOTES
Tested 2/17/18 on OSX 10.13 targeting 10.10 min

## Setup
1. Install Xcode command line tools from http://railsapps.github.io/xcode-command-line-tools.html
2. Use `brew` as the package manager via https://www.howtogeek.com/211541/homebrew-for-os-x-easily-installs-desktop-apps-and-terminal-utilities/

## Dependencies
boost           1.66.0          `brew install boost`
openssl         1.0.2n          `brew install openssl`
miniupnpc       2.0.20180203    `brew install miniupnpc`
qrencode        4.0.0           `brew install qrencode`
qt              5.10.1          `brew install qt5`
berkeley-db@4   4.8.30          `brew install berkeley-db4`
libevent        2.1.8           `brew install libevent`

or all together:
`brew install boost openssl miniupnpc qrencode qt5 berkeley-db4 libevent`

## Build MotaCoin-Qt.app
1. Run `qmake` to create Makefile from MotaCoin-qt.pro
2. Run `make`
