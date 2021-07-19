# Installing Python on Windows

The first step to using python on windows is to install it. The recommended installation method on windows is to install it directly from the Python website, https://www.python.org/downloads/. You can install Python from the Microsoft Store, I would not recommend it as it has been known to cause issues with some modules, and the install offers less configuration options.

Installing the latest version will give you access to Python's newest features and updates, however if you are planning to use some particular modules, it is worth checking they support that version. It is recommended that you install 64-bit python if your computer supports it, unless you have reason not to.

When you run the installer you should first see a screen like this:

![python_installer_screen](https://user-images.githubusercontent.com/22353562/126144479-cfe6bd98-6d2e-47c3-b6b3-5de9f2656e9a.png)

First you should tick "Add Python x to PATH", this is important as it allows you to access your installation using the `python` command in your terminal. If you want to install multiple python versions you may not want to do this for all versions, see <insert guide here> for more on that.
  
If you would like to install Python locally (just for your user account), you can press "install now" to run the installation. However, unless you either 1) do not have admin permissions on the device you are using, or 2) are on a computer multiple people use and don't want to install Python for all accounts, I would recommend installing globally. To do this, click "Customize installation". You should then see a screen like this:
  
![WindowsSandboxClient_E4oGagmzqS](https://user-images.githubusercontent.com/22353562/126212451-a6fe7fee-9c80-4c13-91d3-3c61f871aed7.png)
  
All the settings here are fine so can be left ticked, now click "next". You should see a screen like this:
  
![msNF4SmSu3](https://user-images.githubusercontent.com/22353562/126213053-a2cc3b58-0a2c-4e97-a30c-e3ed878e232b.png)
  
Here you can select "Install for all Users". Then click install, and you're done!
  
To test your installation you can try opening a new terminal (type "cmd" in the windows search bar to open one), typing `python -V`, and pressing enter.
  
  
  
