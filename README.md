# JormoCoin: Version 2

Cryptocurrencies today are starting to be less and less about mining. Thats why I made up with Jormo. I want there to be a coin that is focused on mining and community. We use Cryptonight V7 Lite to create an ASIC resistant coin. This way everyone can enjoy the coin and not have to worry about an overload caused by ASIC's. Our development team is dedicated to keeping up on this to make sure ASIC's do not win. We picked this time to release our coin because most currencies are switching to V7 Lite which will change how their coin works. While Jormo is being released with V7 Lite so it is in Jormo's bones.

To get started download the source and compile it. There are tutorials below to show you how to compile on your platform. Then download a miner like xmr-stak or xmrig and connect to the official mining pool (https://pool.jormo.org). If you are more of a solo miner you can use the miner tool located in `Jormo/build/src`.

### Links and Resources

As said above one of our goals is to focus on community. The best way to talk with the community is to join the discord (https://discord.gg/4ZA8dRY) or subreddit (https://www.reddit.com/r/Jormo/). These resources can also be used to ask for help or suggest new features or ideas. If you notice a bug or get an error post an issue on the github issue page (https://github.com/JormoCoin/JormoV2/issues/). This is the best way to get problems solved fast.

To get instant updates on development, plans, new versions, or any other sorts of news follow us on Twitter @JormoCoin.

We are not liable for anything that happens or is done with our project! There is no warranty on this project!

### How To Compile

If you do not want to compile there is a GUI wallet you can find here: https://github.com/JormoCoin/GUIWallet.

#### Ubuntu 16.04+ and MacOS 10.10+

##### Prerequisites

- You will need the following packages: boost (1.55 or higher), rocksdb, cmake, git, gcc (4.9 or higher), g++ (4.9 or higher), make, and python. Most of these should already be installed on your system.
- For example on Ubuntu: `sudo apt-get install -y build-essential python-dev gcc g++ git cmake libboost-all-dev librocksdb-dev`
- If you are using Ubuntu and your version of Ubuntu doesn't have librocksdb-dev, you can get it from a ppa instead:
```
sudo add-apt-repository ppa:ethcore/ethcore -y
sudo apt-get update
sudo apt-get install librocksdb-dev
```

##### Building

- `git clone https://github.com/JormoCoin/JormoV2`
- `cd JormoV2`
- `mkdir build && cd $_`
- `cmake ..`
- `make`

#### Apple

##### Prerequisites

- Install [cmake](https://cmake.org/). See [here](https://stackoverflow.com/questions/23849962/cmake-installer-for-mac-fails-to-create-usr-bin-symlinks) if you are unable call `cmake` from the terminal after installing.
- Install the [boost](http://www.boost.org/) libraries. Either compile boost manually or run `brew install boost`.
- Install XCode and Developer Tools.

##### Building

- `git clone https://github.com/JormoCoin/JormoV2`
- `cd JormoV2`
- `mkdir build && cd $_`
- `cmake ..` or `cmake -DBOOST_ROOT=<path_to_boost_install> ..` when building
  from a specific boost install. If you used brew to install boost, your path is most likely `/usr/local/include/boost.`
- `make`

The binaries will be in `./src` after compilation is complete.

Run `./build/src/TurtleCoind` to connect to the network and let it sync (it may take a while).

#### Windows 10

##### Prerequisites
- Install [Visual Studio 2017 Community Edition](https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=Community&rel=15&page=inlineinstall)
- When installing Visual Studio, it is **required** that you install **Desktop development with C++** and the **VC++ v140 toolchain** when selecting features. The option to install the v140 toolchain can be found by expanding the "Desktop development with C++" node on the right. You will need this for the project to build correctly.
- Install [Boost 1.59.0](https://sourceforge.net/projects/boost/files/boost-binaries/1.59.0/), ensuring you download the installer for MSVC 14.

##### Building

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017'.
- `cd <your_turtlecoin_directory>`
- `mkdir build`
- `cd build`
- Set the PATH variable for cmake: ie. `set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%`
- `cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=C:/local/boost_1_59_0` (Or your boost installed dir.)
- `MSBuild TurtleCoin.sln /p:Configuration=Release /m`
- If all went well, it will complete successfully, and you will find all your binaries in the '..\build\src\Release' directory.
- Additionally, a `.sln` file will have been created in the `build` directory. If you wish to open the project in Visual Studio with this, you can.

## Apology

For those of you that participated in the original Jormo I apologize greatly for making your mining pointless. As some of you might know I was having trouble building a wallet for the old one. This new one has the wallet made on release, there is a paper wallet which was previously not possible. Many more features too.
