# Managing Multiple Python Versions on Windows

Once you start using Python more regularly and try out different projects/modules, you may find yourself wanting (or needing) to work with different Python versions on one computer.

## The py launcher
The Python installer comes with a neat little windows specific tool called the py launcher. It is a command line tool you invoke using the `py` command that you can use to invoke any python version you have installed. Let's take a look at the arguments it takes:
```
Launcher arguments:

-2     : Launch the latest Python 2.x version
-3     : Launch the latest Python 3.x version
-X.Y   : Launch the specified Python version
     The above all default to 64 bit if a matching 64 bit python is present.
-X.Y-32: Launch the specified 32bit Python version
-X-32  : Launch the latest 32bit Python X version
-X.Y-64: Launch the specified 64bit Python version
-X-64  : Launch the latest 64bit Python X version
-0  --list       : List the available pythons
-0p --list-paths : List with paths
```

We'll start from the bottom, with the very useful `py -0p` command. This lists the python versions you have installed, the output will look something like this:
```
C:\Users\WDAGUtilityAccount>py -0p
Installed Pythons found by py Launcher for Windows
 -3.9-64        C:\Program Files\Python38\python.exe *
 -3.8-64        C:\Program Files\Python38\python.exe
 -3.7-64        C:\Program Files\Python37\python.exe
```
The versions will be ordered from newest to oldest, and the `*` will indicate which version running `py` will call by default. This depends on the following requirements, and may not be the same version you get from running `python` (if you get any):
```
If an exact version is not given, using the latest version can be overridden by
any of the following, (in priority order):
 • An active virtual environment
 • A shebang line in the script (if present)
 • With -2 or -3 flag a matching PY_PYTHON2 or PY_PYTHON3 Environment variable
 • A PY_PYTHON Environment variable
 • From [defaults] in py.ini in your %LOCALAPPDATA%\py.ini
 • From [defaults] in py.ini beside py.exe (use `where py` to locate)
```

You can override which version is called by specifying the major and minor versions to used. For example, to invoke python 3.7, you could run `py -3.7`. You can then pass any arguments to `python` on top of that, for example `py -3.7 myscript.py` to run `myscript.py`, or `py -3.7 -m pip install numpy` to invoke `pip` to install numpy into that version.

You can use `py` instead of `python` and not have any python versions on path at all, but personally I would recommend having your "main" python version on path so you can invoke it with `python` if you want to.

## Virtual Environments

I wont aim to explain how to work with venvs fully here, as that's a pretty big topic, but it's important to mention. Virtual environments, commonly abbreviated `venvs`, are a way of letting each of your projects run in it's own python environment, so you can have different projects with different versions of the same depencencies. This fits in closely with managing different Python versions, as different projects may require different Python versions. If your editor/IDE has builtin support for managing venvs, I would recommend you find docs/a tutorial specific to that. Here's a [VSCode tutorial](https://code.visualstudio.com/docs/python/environments), and here's [one for Pycharm](https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html). [Poetry](https://python-poetry.org/) and [Pipenv](https://pipenv.pypa.io/en/latest/) are both popular tools for managing dependencies
