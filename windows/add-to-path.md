# Adding Python to PATH

If, when trying to use the `python` or `pip` commands in your console, you get an error message saying the command is not recognised, or you don't get any output at all, it is likely that you didn't add Python to PATH when installing it.

PATH is "the system variable that your operating system uses to locate needed executables from the command line or Terminal window.", so whenever you type a command in your terminal, the terminal will look it up in the PATH to try and find out what program that command refers to, so it can execute it. The Python installer does not add Python to path by default, but even if you forgot to add it when installing, it is easy to change.

## How?

Some tutorials would advise going into your environment variables and editing your PATH manually, however it can be done more easily and safely directly from the installer. Here is how to do that.

1) Search for "apps and features" in the windows search bar
2) In the "app list" search bar search for "python":

![ApplicationFrameHost_RZlL6JxpXK](https://user-images.githubusercontent.com/22353562/126302189-24768d69-5bec-44d4-bfa3-7d109c3e29f7.png)
  
3) Find the version you want to add to path, click the three dots next to the name, and select "modify". This should open up a window like this: 

![WindowsSandboxClient_5oRm5PTNiO](https://user-images.githubusercontent.com/22353562/126303153-af573676-a143-4da4-bf78-eba0a4154615.png)

4) Select "modify", and then click "next" on the "Optional Features" screen.
5) On the "Advanced Options" screen, tick the "Add Python to environment variables" checkbox:

![NkeEczCt2U](https://user-images.githubusercontent.com/22353562/126303895-60155ea5-7189-4924-9aa7-de696ca02ae9.png)

7) Click install, close and reopen the terminal you are using / restart your code editor if you're using its terminal, and test it has worked by running `python -VV`.


You should now have added Python to your PATH successfully! Please let me know if you had any problems following this guide or have any other feedback.



