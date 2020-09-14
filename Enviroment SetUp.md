# Enviroment SetUp  

* [Windows 10](https://hackmd.io/C77OMqfuSUGuf-SDC0zUwA#Windows-10)
* [Ubuntu](https://hackmd.io/C77OMqfuSUGuf-SDC0zUwA#UbuntuUbuntu-on-Window-10)
* [MacOS](https://hackmd.io/C77OMqfuSUGuf-SDC0zUwA#MacOS)

## Windows 10  
### 1. Open developer mode on window  
![](https://i.imgur.com/90z86U2.png)  
![](https://i.imgur.com/2mP5opN.png)  

### 2. Enable Linux version Windows sub system.  
![](https://i.imgur.com/dZ695aE.png)  
![](https://i.imgur.com/ZfGTY1D.png)  

### 3. Install Ubuntu on Microsoft Store and activate it.
![](https://i.imgur.com/oSL9INK.png)

### 4. Now you can open bash shell in cmd.  
![](https://i.imgur.com/v7WVbMe.png)

## Ubuntu(Ubuntu on Window 10)  
### 1. Run the following command under bash shell.  
```
sudo apt-get update
sudo apt-get install g++
sudo apt-get install make
sudo apt-get install libgtest-dev
sudo apt-get install cmake
cd /usr/src/gtest 
sudo cmake CMakeLists.txt 
sudo make 
sudo cp *.a /usr/lib
```

## MacOS  

### 1. Download [GoogleTest](https://github.com/google/googletest/releases/tag/release-1.10.0) and run the following command.  
```
brew install cmake
cd ~/Downloads/googletest-release-1.10.0/googletest
mkdir build
cd build
cmake –Dgtest_build_samples=ON –Dgtest_build_tests=ON ~/Downloads/googletest-release-1.10.0/googletest
make
sudo mkdir /usr/local/Cellar/gtest
sudo cp ~/Downloads/googletest-release-1.10.0/googletest/build/libgtest.a /usr/local/Cellar/gtest/
sudo ln –snf /usr/local/Cellar/gtest/libgtest.a /usr/local/lib/libgtest.a
sudo cp –r ~/Downloads/googletest-release-1.10.0/googletest/include /usr/local/Cellar/gtest/
ln –snf /usr/local/Cellar/gtest/include/gtest /usr/local/include/gtest
```