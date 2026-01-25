# Setting up the Environment

For this class, I recommend using Conda combined with Visual Studio Code. I believe this to be the easiest and fastest setup across all platforms.

## Choose Your Operating System

Click on the link that matches your operating system:

- [I will use Linux](i_will_use_linux.md)
- [I will use Windows](i_will_use_microsoft.md)
- [I will use macOS](I_will_use_macos.md)

---

## Defining the Work Environment in VSCode

Now, let's prepare our VSCode setup. These steps apply to Linux, Windows, and macOS.

**Note for macOS users:** Replace `Ctrl` with `Cmd` for keyboard shortcuts (e.g., `Cmd + Shift + P` instead of `Ctrl + Shift + P`).

1. First, create a folder for our first project and open it in VSCode.

2. Next, set up our Conda environment in VSCode. Press `Ctrl + Shift + P`, type `select interpreter`, and choose the `base` environment. To check if it's working, open a new terminal from "Terminal" -> "New Terminal". If it's working, you'll see `(base)` at the beginning of your terminal prompt. Try a simple "hello world" program to test.

3. VSCode offers helpful extensions. Install the following:
   - Python
   - Pylance
   - Jupyter

4. Test our Jupyter notebook setup by creating a `test.ipynb` file. Try executing a cell with a simple Python command (use `Ctrl + Enter`). VSCode will prompt you to select the Python interpreter again. Choose `base`. You may be asked to install `Ipykernel`. After installation, you should be able to run Jupyter cells.


Congratulations! You now have a functional environment with VSCode, Jupyter, and the necessary tools!
