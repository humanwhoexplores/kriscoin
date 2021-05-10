Kriscoin Core 0.14.2
=====================

Setup
---------------------
Kriscoin Core is the original Kriscoin client and it builds the backbone of the network. However, it downloads and stores the entire history of Kriscoin transactions (which is currently several GBs); depending on the speed of your computer and network connection, the synchronization process can take anywhere from a few hours to a day or more.

To download Kriscoin Core, visit [kriscoin.org](https://kriscoin.org).

Running
---------------------
The following are some helpful notes on how to run Kriscoin on your native platform.

### Unix

Unpack the files into a directory and run:

- `bin/kriscoin-qt` (GUI) or
- `bin/kriscoind` (headless)

### Windows

Unpack the files into a directory, and then run kriscoin-qt.exe.

### OS X

Drag Kriscoin-Core to your applications folder, and then run Kriscoin-Core.

### Need Help?

* See the documentation at the [Kriscoin Wiki](https://kriscoin.info/)
for help and more information.
* Ask for help on [#kriscoin](http://webchat.freenode.net?channels=kriscoin) on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net?channels=kriscoin).
* Ask for help on the [KriscoinTalk](https://kriscointalk.io/) forums.

Building
---------------------
The following are developer notes on how to build Kriscoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

- [OS X Build Notes](build-osx.md)
- [Unix Build Notes](build-unix.md)
- [Windows Build Notes](build-windows.md)
- [OpenBSD Build Notes](build-openbsd.md)
- [Gitian Building Guide](gitian-building.md)

Development
---------------------
The Kriscoin repo's [root README](/README.md) contains relevant information on the development process and automated testing.

- [Developer Notes](developer-notes.md)
- [Release Notes](release-notes.md)
- [Release Process](release-process.md)
- [Source Code Documentation (External Link)](https://dev.visucore.com/kriscoin/doxygen/)
- [Translation Process](translation_process.md)
- [Translation Strings Policy](translation_strings_policy.md)
- [Travis CI](travis-ci.md)
- [Unauthenticated REST Interface](REST-interface.md)
- [Shared Libraries](shared-libraries.md)
- [BIPS](bips.md)
- [Dnsseed Policy](dnsseed-policy.md)
- [Benchmarking](benchmarking.md)

### Resources
* Discuss on the [KriscoinTalk](https://kriscointalk.io/) forums.
* Discuss general Kriscoin development on #kriscoin-dev on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net/?channels=kriscoin-dev).

### Miscellaneous
- [Assets Attribution](assets-attribution.md)
- [Files](files.md)
- [Fuzz-testing](fuzzing.md)
- [Reduce Traffic](reduce-traffic.md)
- [Tor Support](tor.md)
- [Init Scripts (systemd/upstart/openrc)](init.md)
- [ZMQ](zmq.md)

License
---------------------
Distributed under the [MIT software license](/COPYING).
This product includes software developed by the OpenSSL Project for use in the [OpenSSL Toolkit](https://www.openssl.org/). This product includes
cryptographic software written by Eric Young ([eay@cryptsoft.com](mailto:eay@cryptsoft.com)), and UPnP software written by Thomas Bernard.
