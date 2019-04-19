# Prep Jekyll development environment on your computer:

## 1. Install Git 

**Windows:** install [Git for Windows](https://git-for-windows.github.io/) (this does *NOT* require admin access). 
This will give you Git, Git Bash, and Git GUI.
Git Bash is a great terminal that lets you use UNIX style commands and utilities on Windows.

- Download the current installer from [Git for Windows](https://git-for-windows.github.io/)
- Double click the file (something like `Git-2.19.1-64-bit.exe`) to start the installer. If you computer gives a warning (such as "Do you want to run this file?"), click "Run" or okay. 
- Click through the installer using the default options, except when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default".
- Installation may take a minute to complete. 

Other OS:

- **Mac:** check if Git is already installed by opening terminal and typing `git --version`. If you do not have it, your system will often prompt you to install "Xcode Command Line Tools"--follow the prompt as this package is necessary for Ruby as well. Alternatively, type `xcode-select --install` to start the process. If you want a newer version, download the official [Mac git installer](https://git-scm.com/downloads) or use Homebrew.
- **Linux:** install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

## 2. Install GitHub Desktop

Windows and Mac users can also install [GitHub Desktop](https://desktop.github.com/), a GUI tool to work with Git repositories and GitHub (this does *NOT* require admin access).

- Download the installer from [GitHub Desktop](https://desktop.github.com/)
- Double click the file (something like `GitHubDesktopSetup.exe`) to start the installer, follow all the default options.
- Log in with your GitHub username and password.

## 3. Install Text Editor

A good text editor is essential for working with code. 
Since Jekyll projects are a bundle of interconnected folders and text files, it is easiest to use an editor that has a file explorer, a terminal, and git built in.
Most of us use [Visual Studio Code](https://code.visualstudio.com/) (this does *NOT* require admin access).

- Download installer from [Visual Studio Code](https://code.visualstudio.com/)
- Double click the file (something like `VSCodeUserSetup-x64-1.29.1.exe`) to start the installer, follow the default options.
- Open Code and click File > Preferences > Settings to customize the options. 
- Open a terminal window by clicking Ctrl + backtick/~. In the terminal window look for an option to customize which terminal is used--select Git Bash from the drop down. Alternatively, set this option in the Preferences.
- Add spell check: click on the extensions icon (square on left side), search for "code spell checker", click install.

## 4. Install Ruby 

**Windows:** Use [RubyInstaller for Windows](https://rubyinstaller.org/) (this does *NOT* require admin access). 

- [Download](https://rubyinstaller.org/downloads/) the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.5.X (x64))
- Double click the file (something like ``) to start the installer, use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
- When complete, the installer will open a terminal window with options to install the MSYS2 DevKit components. Simply press Enter (or choose option 3, "MSYS2 and MINGW development toolchain") to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window--*eventually*, this will conclude and you should see a message with success in it. If the window doesn't close, press Enter again or manually close it. (This installer can be restarted by typing `ridk install` into a command prompt)

**Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.2.5 you can use the system Ruby, but it is better to install a non-system version using a manager. Check the official Jekyll [Mac install docs](https://jekyllrb.com/docs/installation/macos/) for tips. 

- Ensure you have Xcode Command Line Tools, if not use `xcode-select --install` to start the installer.
- Install manager [RVM](https://rvm.io/) using helper:
    - Install gpg2, using [Homebrew](https://brew.sh/), `brew install gnupg`
    - Get the public key: `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
    - Get the helper script and install: `\curl -sSL https://get.rvm.io | bash -s stable`
- Install recent stable version of Ruby:
    - Check [Ruby Downloads](https://www.ruby-lang.org/en/downloads/) for number of "current stable version", currently 2.5.3
    - Use RVM to install that version: `rvm install 2.5.3` (this may take a long time...)
    - Set it as default Ruby: `rvm use 2.5.3`
    - Check: `ruby -v`
- Alternatively, some people supposedly have success using [Homebrew](https://brew.sh/) (`brew install ruby`) or another manager such as [rbenv](https://github.com/rbenv/rbenv) (although experience suggests RVM is best option).

**Linux:** The simplest method is to use your distro's repositories (e.g. `sudo apt install ruby-full`), however it is probably better to use a version manager. Check `ruby -v` to make sure the repository version is > 2.2.5. See the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/) for more details.

- Ensure you have standard build tools (Make and GCC), on Ubuntu get them with `sudo apt install build-essential`.
- Install manager [RVM](https://rvm.io/) (this might require a terminal tweak, see [Ubuntu tips](https://evanwill.github.io/_drafts/notes/ruby-notes.html))
- Install recent stable version of Ruby:
    - Check [Ruby Downloads](https://www.ruby-lang.org/en/downloads/) for number of "current stable version", currently 2.5.3
    - Use RVM to install that version: `rvm install 2.5.3` (this may take a long time...)
    - Set it as default Ruby: `rvm use 2.5.3`
    - Check: `ruby -v`

## 5. Install Jekyll 

Open a new Git Bash/terminal window and type:

`gem install jekyll bundler`

On Windows this may take a few minutes and look like nothing is happening--but eventually it will complete and give some output saying it was successful.
Check your install by typing:

`jekyll -v`
