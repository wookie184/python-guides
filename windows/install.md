# Installing Python on Windows

The recommended installation method on windows is to install it directly from the Python website, https://www.python.org/downloads/.

You *can* install Python from the Microsoft Store, although I would not recommend it as it has been known to cause issues with some modules, and the install offers less options for install configuration.

### Which version?
**Recommended**: latest or second latest

**Details**:  
Installing the latest version will give you access to Python's newest features and updates, however some modules may not support the newest versions straight away, so it may be worth going with the second newest. If you find you want some newer features or your module does not support your current version, you can always install another version, check out [this guide](https://github.com/wookie184/python-guides/blob/main/windows/managing-multiple-versions.md) for more on that.

### 32-bit vs 64-bit?
**Recommended**: 64-bit

**Details**:  
It is recommended that you install 64-bit python if your computer supports it, unless you have reason not to. With 32 bit you may run into memory limits if doing intensive operations (Python will be limited to using 4GB of memory), and some modules may not offer prebuilt wheels for 32 bit when installing modules, potentially meaning installs may be slower or you may have to install build dependencies.

To find out if your computer supports 64 bit Python, search "About your PC" in windows search and open the settings page. Then look for the "System Type" option under "Device Specifications". It should say "64-bit operating system, x64-based processor" if you have support. You need a 64 bit processor and OS to install 64 bit programs.

### Add to PATH, or not?
**Recommended**: Yes, do add to PATH

**Details**:  
If you're installing Python for the first time you'll probably want to add Python to PATH. This allows you to access your installation using the `python` and `pip` commands in your terminal to invoke Python.

You may not want to do this are if you are installing a secondary version, see [this guide](https://github.com/wookie184/python-guides/blob/main/windows/managing-multiple-versions.md) for more on how you can manage that without adding to PATH.

If you installed Python without adding to PATH and now want to do so, check out [this guide](https://github.com/wookie184/python-guides/blob/main/windows/add-to-path.md)

### Global or Local installation?
**Recommended**: Global, although it shouldn't matter much

**Details**:
This doesn't matter much, although I prefer installing globally as it gives a shorter path to the Python executable, and sometimes I may log into a different user account and want to access Python.

If you either do not have admin permissions on the device you are using, or are on a computer multiple people use and don't want to install Python for all accounts, you should install locally.


## Running the installer
When you run the installer you should first see a screen like this:

![python_installer_screen](https://user-images.githubusercontent.com/22353562/126144479-cfe6bd98-6d2e-47c3-b6b3-5de9f2656e9a.png)

If you want to add to PATH, be sure to tick the "Add Python X.X to PATH" checkbox.
  
If you would like to install Python locally you can press "install now" to run the installation, and you are done! If you would like to install globally, click "Customize installation". You should then see a screen like this:
  
![WindowsSandboxClient_E4oGagmzqS](https://user-images.githubusercontent.com/22353562/126212451-a6fe7fee-9c80-4c13-91d3-3c61f871aed7.png)
  
All the settings here are fine so can be left ticked, now click "next". You should see a screen like this:
  
![msNF4SmSu3](https://user-images.githubusercontent.com/22353562/126213053-a2cc3b58-0a2c-4e97-a30c-e3ed878e232b.png)
  
Here you can select "Install for all Users". Then click install, and you're done!
  
To test your installation you can open a new terminal (type "cmd" in the windows search bar and select "Command Prompt"), type `python -V`, and press enter.
  
  

  
