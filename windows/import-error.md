# Solving Import Errors

An import error suggests that python cannot find the module you are trying to `import`, and can happen for many reasons. This guide focusses on helping debug external modules that you install from PyPI using `pip`

### Are you actually getting an ImportError?
If you are using a code editor such as VSCode or Pycharm you may get a squiggly line under your import saying the module couldn't be found, it is possible that this is just an mistake by the editor, so you should try running your code with python to check that it can't find the file.

If your code runs fine, you could try restarting your editor - if you have newly installed a module it may just not have recognised that yet. You may also need to configure it to ensure it is pointing to the correct python executable, you should search up your editor to double check this.

### Did you use the correct module name?
Double check that you haven't made a typo in the name you are importing, or in what you installed from PyPI, you need to make sure you get the name exactly as it should be.

Also check that the name you are using in the `import` is correct, **it may not be the same as the name you `pip install`**. Check the docs or PyPI page if you are unsure.
Examples of this are:
* [**opencv-python**](https://pypi.org/project/opencv-python/): You need to `pip install opencv-python`, but the import has to be `import cv2`
* [**discord.py**](https://pypi.org/project/discord.py/): You need to `pip install discord.py`, but the import has to be `import discord`
* [**python-dotenv**](https://pypi.org/project/python-dotenv/): You need to `pip install python-dotenv`, but the import has to be `import dotenv`

### Are you installing to the wrong python executable?
This is a very common problem, and can be difficult to fix as there are many ways it can happen. When you install a module from PyPI, you will install it into a single python executable, the one that the `pip` you invoked is referring to. This could be different to the one you are running the script from, usually because it's using a different python version, or a virtual environment.

To debug this, you should first find out if you are using two different versions. An easy way of doing this is by printing out `sys.executable` from the script you are running, and from the python you're installing the module into.

First run `python -c "import sys;print(sys.executable)"` from the same place you did the pip install, and remember the result. You can try `python -m pip install <insert package>` to ensure you're using the same `pip` as the `python` you're checking the executable for.

Then add `import sys;print(sys.executable)` to the top of the code you are running, and run the file as you did before, noting the result.

If the two results are different, you've likely found the source of your problem.

Here are some tips for getting the versions to match:
* If you are running your code in a venv, ensure you have activated your venv before running `pip install`
* If you are running your code through your editor, make sure you have it set up to use the same editor you are `pip install`ing into.
* Use the `py` command to specify the python version you want to pip install into, e.g. `py -3.9 -m pip install numpy`, or to specify.

If you are running your code through your editor or pip installing through your editor, you should check its docs for more information. Here are some useful links:
* **VSCode**: [Using Python environments in VS Code](https://code.visualstudio.com/docs/python/environments)
* **PyCharm**: [Configuring a Python interpreter](https://www.jetbrains.com/help/pycharm/configuring-python-interpreter.html)
