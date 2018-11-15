# Web Development Tools

> tools and skills to contribute to library websites

## Contribute via GitHub web interface 

- Create professional [GitHub account](https://github.com/join)
- Join [uidaholib](https://github.com/uidaholib) organization and Web Team. An admin will invite you, but you must accept the invitations.
- Familiarize with GitHub interface, [Hello World guide](https://guides.github.com/activities/hello-world/).
- Learn [Markdown](https://daringfireball.net/projects/markdown/) basics, [Mastering Markdown guide](https://guides.github.com/features/mastering-markdown/)
- Familiarize with [HTML](https://www.w3schools.com/html/default.asp) and [Bootstrap 4](https://getbootstrap.com/docs/4.1/getting-started/introduction/) basics
- Familiarize with basics of [Jekyll](https://jekyllrb.com/)
- Understand how to add relative links using Liquid
- Understand organization of website project

## Develop locally and push to contribute

### Prep development environment on your computer:

#### 1. Install Text Editor

Most of us use [Visual Studio Code](https://code.visualstudio.com/).

#### 2. Install Git 

- **Windows:** install [Git for Windows](https://git-for-windows.github.io/) using the default options, except when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a great terminal that lets you use UNIX style commands and utilities on Windows.
- **Mac:** check if Git is already installed by opening terminal and typing `git --version`. If you do not have it, your system will often prompt you to install "Xcode Command Line Tools"--follow the prompt as this package is necessary for Ruby as well. Alternatively, type `xcode-select --install` to start the process. If you want a newer version, download the official [Mac git installer](https://git-scm.com/downloads) or use Homebrew.
- **Linux:** install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

#### 3. Install GitHub Desktop

Windows and Mac users can also install [GitHub Desktop](https://desktop.github.com/) using the default options.

#### 4. Install Ruby 

- **Windows:** Use [RubyInstaller for Windows](https://rubyinstaller.org/). 
    - First, [download](https://rubyinstaller.org/downloads/) the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 2.5.X (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
    - Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. (This installer can be restarted by typing `ridk install` into a command prompt)
- **Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.2.5 you can use the system Ruby. 
    - A newer version can be installed using [Homebrew](https://brew.sh/){:target="_blank"}, `brew install ruby`, or a manager such as [rbenv](https://github.com/rbenv/rbenv){:target="_blank"}. Check the official Jekyll [Mac install docs](https://jekyllrb.com/docs/installation/macos/){:target="_blank"} for tips. 
    - Ensure you have Xcode Command Line Tools, if not use `xcode-select --install` to start the installer.
- **Linux:** Even though the version will not be the most up-to-date, the simplest method is to use your distro's repositories. For example on Ubuntu, `sudo apt install ruby-full`. Check `ruby -v` to make sure the repository version is > 2.2.5. See the official Jekyll [Ubuntu install docs](https://jekyllrb.com/docs/installation/ubuntu/){:target="_blank"} for more details.
    - For a more up-to-date version, use a manager such as [RVM](http://rvm.io/){:target="_blank"} ([Ubuntu tips](https://evanwill.github.io/_drafts/notes/ruby-notes.html){:target="_blank"})
    - You will also need some build tools (Make and GCC), on Ubuntu get them with `sudo apt install build-essential`.

#### 5. Install Jekyll 

Open a terminal/Git Bash and type:

`gem install jekyll bundler`

### Skills

- Understand Jekyll concepts and project organization
- Understand `jekyll s`
- Understand [GitHub Flow](https://guides.github.com/introduction/flow/) to make contributions
- Understand local conventions and standards 

## Build and manage website

- Understand `jekyll build`
- Have access to web server
