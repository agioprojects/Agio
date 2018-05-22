# Agio

This is the reference code for [Agio](https://) cryptocurrency.

* Official homepage: [Agio](http://)
* Official repository: [Agio GitHub](https://github.com/agioprojects/agio)
* Official Announcement thread: [Agio BitcoinTalk](https://)
* Official Discord: [Agio Discord](https://discord.gg/)
* Official Facebook: [Agio Facebook](https://www.facebook.com/)
* Official Twitter: [Agio Twitter](https://twitter.com/)
* Official Telegram: [Agio Telegram](https://t.me/joinchat/)
* Official Whitepaper: [Agio Whitepaper](http://)
* Official Block explorer: [Agio Block explorer](http://)


## Agio Cryptocurrency

Agio [AGIO] is an ASIC resistant CryptoNightLite V1 algorithm based cryptocurrency. Fast transactions & privacy make this coin perfect for rewarding your workers, co-workers and colleagues for a job well done.

- Algorithm: CryptoNightLite V1
- Max. supply: 1,000,000,000.
- CryptoNote name: agio
- Decimal points: 8
- Block time: 120
- Ticker: AGIO
- Emission speed factor: 21
- P2P port: 11212
- RPC port: 11213

## How to compile

### Compile on Linux Ubuntu 16

**1. Install dependencies**

- run an update

``
sudo apt-get update
``

- get all dependencies

``
sudo apt-get install build-essential python-dev gcc g++ git cmake librocksdb-dev libboost-all-dev
``

**2. Get the coin**

``
git clone https://github.com/agioprojects/agio.git agio
``

**3. CHMOD**

- navigate to:

``
cd agio/external/rocksdb/build_tools
``

- execute the following commands:

``
chmod +x build_detect_platform
``

``
chmod +x version.sh
``

**4. Build executables**

- Navigate back to repo folder 

``
cd
``

``
cd agio
``

- prepare the build

``
mkdir build && cd $_
``

``
cmake ..
``

- Export flags

``
export CXXFLAGS="-std=gnu++11"
``

- Make/Build

``
make
``

_Your executables will be located in `build/src` folder._


### Compile on Linux Ubuntu 14

**1. Install dependencies**

- run an update

``
sudo apt-get update
``

- get all dependencies

``
sudo apt-get install -y build-essential python-dev git cmake libboost1.55-all-dev libgflags-dev libsnappy-dev zlib1g-dev libbz2-dev libgflags-dev libgflags2 gcc-4.8 g++-4.8
``

**2. Install RocksDB database (long compilation)**

``
git clone https://github.com/facebook/rocksdb.git
``

``
cd rocksdb
``

``
make all
``

**3. Get the coin**

``
cd
``

``
git clone https://github.com/agioprojects/agio.git agio
``

**4. CHMOD**

- navigate to:

``
cd agio/external/rocksdb/build_tools
``

- execute the following commands:

``
chmod +x build_detect_platform
``

``
chmod +x version.sh
``

**5. Build executables (long compilation)**

- Navigate back to repo folder 

``
cd
``

``
cd agio
``

- prepare the build

``
mkdir build && cd $_
``

``
cmake ..
``

- Export flags

``
export CXXFLAGS="-std=gnu++11"
``

- Make/Build

``
make
``

### Compile on Windows 7/8/10

**1. Environment**

- Visual Studio 2017 Community Edition with desktop development with C++ and the VC++ v140 toolchain features selected
- Boost 1.59.0, with the installer for MSVC 14

**2. Build**

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017'


``
cd <agio_directory>
``

``
mkdir build
``

``
cd build
``


-  Set the PATH for Cmake:

``
set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%
``

- Run Cmake:

``
cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=C:/local/boost_1_59_0
``

- Build:

``
MSBuild agio.sln /p:Configuration=Release /m
``

_Your binaries  will be located in `..\build\src\Release` folder._


### Credits
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Developers, Worktips Developer
