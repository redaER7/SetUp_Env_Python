# Set Up Python environment
* [Install on MacOS](#Install-on-MacOS)
* [Install on Linux](#Install-on-Linux)
* [Install on Windows](#Install-on-Windows)

Mac OS X comes with Python 2.7 already.

These instructions concern the installation of Python3.

The version shipped with OS X may be out of date from the official current Python release, which is considered the stable production version.

# Install on MacOS
## Install Xcode
Before installing Python3, We need to install Xcode.
the Xcode Command Line Tools package gives you a complete Unix toolkit accessible through Terminal.

Within the Xcode Command Line toolkit, Mac users gain access to numerous useful tools, utilities, and compilers, including make, GCC, clang, perl, svn, git, size, strip, strings, libtool, cpp, and many others. All of these commands are a default part of Linux systems and programs. 

1. Open Terminal from searchbar or Go to Terminal in /Applications/Utilities/.
2. Input the following command string in Terminal: 
```
$ xcode-select --install
```
3. A popup update window will appear asking you: “The xcode-select command requires the command line developer tools. Would you like to install the tools now?” click yes and continue.

## Install Homebrew
Homebrew is a package manager for macOS which lets you install free and open-source software using your terminal. You’ll use Homebrew to install developer tools like Python, Ruby, Node.js, and more.

1. In terminal, download homebrew package
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
The installation script will explain what it will do and will prompt you to confirm that you want to do it. This lets you know exactly what Homebrew is going to do to your system before you let it proceed. It also ensures you have the prerequisites in place before it continues.

Press the letter `y` for “yes” whenever you are prompted to confirm the installation.

Once the installation process is complete, you will want to put the directory Homebrew uses to store its executables at the front of the PATH environment variable. This ensures that Homebrew installations will be called over the tools that macOS includes.

The file you’ll modify depends on which shell you’re using. If you’re using Bash, you’ll use the file `~/.bash_profile`:
```
nano ~/.bash_profile
```
you may use `vim` instead of `nano` or any other editing package.

However, if you’re using ZSH, you’ll open the file `~/.zshrc`.
```
nano ~/.zshrc
```
Once the file opens up in the Terminal window, add the following lines to the end of the file:
```
# Add Homebrew's executable directory to the front of the PATH
export PATH=/usr/local/bin:$PATH
```
The first line is a comment which helps you remember what this does if you open this file in the future.

To save your changes, hold down the `CTRL` key and the letter `O`, and when prompted, press the `RETURN` key. Then exit the editor by holding the `CTRL` key and pressing `X`. This will return you to your Terminal prompt.

For `vim` , just type `:wq` followed by `ECHAP` button.

To activate these changes, use the `source` command to load the file you modified.

If you modified `.bash_profile`, execute this command:
```
$ source ~/.bash_profile
``` 
If you modified `.zshrc`, execute this command:
```
$ source ~/.zshrc
```

The changes you have made to the PATH environment variable will take effect. They’ll be set correctly when you log in again in the future, as the configuration file for your shell is executed automatically when you open the Terminal again.

let’s verify that Homebrew is set up correctly. Execute this command:
```
$ brew doctor
```
if installation is successfull, you'll see this message.
```
Output
Your system is ready to brew.
```

if not, run:
```
$ brew update
```

## Install Python

```
$ brew install python
```
This will take somes minutes.

Make sure you have successfully install python.
```
$ python3 --version
```

## Install Pip

PIP is a package management system used to install and manage software packages/libraries written in Python. These files are stored in a large “on-line repository” termed as Python Package Index (PyPI).

pip uses PyPI as the default source for packages and their dependencies.

Dowload `pip` with homebrew:
```
$ brew install pip
```

Make sure you have successfully install python.
```
$ pip3 --version
```
# Install on Linux
## Install Python
The following describes how to install Python3 on Ubuntu Linux machines.
If you are using Ubuntu 16.10 or newer, then you can easily install Python3 with:
```
$ sudo apt-get update
$ sudo apt-get install python
```
If you’re using another version of Ubuntu  or you want to use a more current Python, we recommend using the deadsnakes PPA to install Python 3.8:
```
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt-get update
$ sudo apt-get install python3.8
```
If you are using other Linux distribution, chances are you already have Python 3 pre-installed as well. If not, use your distribution’s package manager. For example on Fedora, you would use dnf:
```
$ sudo dnf install python3
```
Make sure you have successfully install python.
```
$ python3 --version
```

## Install Pip
PIP is a package management system used to install and manage software packages/libraries written in Python. These files are stored in a large “on-line repository” termed as Python Package Index (PyPI).

pip uses PyPI as the default source for packages and their dependencies.
To install pip on Ubuntu, Debian, and Linux Mint:
```
$ sudo apt install python3-pip
```
To install pip on CentOS 8 (and newer), Fedora, and Red Hat:
```
$ sudo dnf install python3
```

Make sure you have successfully install python.
```
$ pip3 --version
```
## Install on Windows
Please follow this tutorial
https://www.tutorialspoint.com/how-to-install-python-in-windows
