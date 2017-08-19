# :wrench: toolbox :hammer:
A compilation of useful resources, links, and shortcuts for learning web development and software engineering in general.

_**Work in Progress**_

### 0. Getting Started
So you want to learn how to do web development? Well, you've (hopefully) come to the right place! Let's jump right in.

#### :computer: Your Machine & Necessary Software

###### Pick a solid text editor

Text editors is where you'll be spending most of your time doing the heavy lifting for your code. This is where the actual magic happens. Any of the below listed editors are fantastic and use by millions of developers around the world. Each also have addons & extensions that you can get to augment their initial functionality!

1. [Atom](https://atom.io) - made by Github
2. [Sublime](https://www.sublimetext.com/)
3. [Visual Studio Code](https://code.visualstudio.com/) - made by Microsoft

> :bulb: If you wanted to get a bit fancy, you could check out [WebStorm](https://www.jetbrains.com/webstorm/) or [IntelliJ](https://www.jetbrains.com/idea/). They have student licenses that you can get for free!

###### Understanding the Command Line

The command line is one of the most powerful tools that you'll have at your disposal while being a developer. Interacting with your machine and your files at a low level is powerful, and you can do a lot of neat stuff inside a command line!

Let's break this out into operating systems!

1. Unix based (Mac OSX & Linux). [Unix based machines](https://www.wikiwand.com/en/Unix) are pretty neat and use a [shell](https://www.wikiwand.com/en/Unix_shell) to interact with the files on a computer in an intimate, low level way. TLDR: You can do cool stuff in the shell that would take hours, days, weeks, to do by hand.
  * OSX - Terminal
    * What the heck is the terminal? [Here's an article that talks a little about it](http://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/).
  * Linux - Command line interface (CLI)
    * What is a CLI? [Here's a quick article explaining what it is](https://www.linux.com/learn/how-use-linux-command-line-basics-cli).

2. Windows based. Windows is kinda crappy in that its command line interface (CLI) isn't very good or user friendly. Therefore, to get a good CLI, you have a couple options!
  * [Gitbash](https://git-for-windows.github.io/) - Recommended
  * [Cygwin](https://www.cygwin.com/)

We'll be interacting with `git` through the command line. Doing so allows us to have exact control over manipulating the versions of our code, and ensuring that when working collaboratively with others, the code that you're working on doesn't conflict with another developer. We'll talk more about `git` in a bit!

Here are some of the most used commands that you'll find yourself using as your interact with the command line more and more.

- `cd` - **C**hange **D**irectory, to switch between the different folders that live on your machine.
> :bulb: The `~` represents your **home** directory. You can navigate here with either `cd` or `cd ~`. If you don't specify a directory, `cd` will default to home. The home directly is normally where a bunch of your default files directories will live, like `Downloads`, `Desktop`, `Documents`, etc.
- `pwd` - **P**rint **W**orking **D**irectory, prints the current directory that your terminal window is in.
- `ls` - **L**i**s**ts the files in your current working directory**.**

##### `git` and Github

Additionally, in the command line, we will be utilizing `git`. [`git`](https://git-scm.com/) is a version control software that helps you keep track of the different versions of your files &ndash; any file &ndash; but widely used to control the versions of code. `git` is the version control software that powers [Github](https://github.com), a widely useful and popular site that the majority of developers depend on to store their code online.

You may be thinking: "Ok I see people use Github, but I don't really get it... Why do I need to care about different versions of coding files?" &ndash; and rightfully so! Why _**should**_ we care about Github and version control?

Allow me to pose a hypothetical &ndash; You're working with a few friends on a coding project, and each of you is adding code here or there to your files. Say you find a nasty bug that your friend wrote and didn't realize left. You spend hours fixing that bug and message your group chat letting them know that you eventually got it. Another friend responds saying that they've already fixed that bug, and that they emailed you the new code an hour ago.

:sweat: :triumph: :sleepy:

Now, allow me to pose another hypothetical. You're using `git` and Github, and see the nasty bug locally on your version of the code. But &ndash; before you begin working on it, you **pull** down the most recent version of the code, and notice that it has already been fixed. You just saved a few hours!

Imagine this system, but on a _much_ bigger level, and not necessarily relating to bugs either. `git` is used to keep different versions separate, so adding new features can be done in an isolated manner, bugs can be fixed and the fixed can immediately change in the main code base, and conflicting code is pointed out before it can ever occur.

So let's try out a few things with `git`! If you're unsure if you have `git` on your machine, try running `git --version`. If you get a version # back, you're good to go! Otherwise you can download git [here](https://git-scm.com/book/en/v1/Getting-Started-Installing-Git).

Here are some useful `git` commands to use!

- `git clone <repo_url>`
  - Clones a repository from Github or any other `git` file hosting site (like Gitlab or Bitbucket).
  - ex: `git clone https://github.com/evanfrawley/toolbox.git`
- `git status`
  - Shows the status of your current, local version of the repository.
- `git branch`
  - Shows the list of branches that you have locally.
  - [branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) are a way to keep track of certain "train-of-thoughts" with your code, so you can create a new feature on it, try to fix a bug, or change small things on the code base, without effecting the primary branch! They're _**super duper**_ useful when coding, and you're encouraged to always work on a "non-master" (aka development) branch, and only make changes to the "master" branch through [pull requests](https://yangsu.github.io/pull-request-tutorial/).
- `git checkout -b <branch name>`
  - Creates a new local branch, and navigates to that new branch.
  - ex: `git checkout -b video-chat` creates and navigates to a new branch called `video-chat`
- `git checkout <branch name>`
  - Navigates to the specified branch name.
  - ex: `git checkout master`, `git checkout video-chat`
- `git add <file name OR .>`
  - ex: `git add .` or `git add src/index.js`
- `git commit -m "<commit message">`
  - ex `git commit -m "Add video chat feature to the main app"`
  > :bulb: Protip: imagine commit messaged to read like this: "When applied to the repository, this commit will _**Add video chat feature to the main app**_." Commit messaged should be present-tense, and not past-tense!

- `git log`
  - See the list of commits in reverse chronological order
- `git diff`
  - Shows the difference between the un-added changes and the most recent commit.
  - :100: Advanced: If you've already `git add`'d your files, you can use `git diff --cached` to see the different between your added files and the most recent commit on your repository.
  - :100: Advanced: If you've already `git commit`'d to your local repository, you can use `git diff <branch name>` to see the difference between your local branch and the branch in question.
- `git push <remote> <branch name>`
  - Pushes your committed changes up to the specified branch.
  - ex: `git push origin master`
  > :bulb: Protip: Nomrally you can just do `git push` and `git` will yell at your to push a certain way. You can just copy paste what it tells you to use and you should be good to go!

- :100: Advanced: `git remote` (& `git remote -v`)
  - Remotes are useful in that they allow you to interact with the _**current**_ repository (and the _**parent**_ repository if your repository is a [fork](https://help.github.com/articles/fork-a-repo/) of another).

These may be a little daunting, but as long as you keep practicing them, the commands and being comfortable with `git` will surely come!

> :books: [Git tutorial by Github](https://try.github.io/levels/1/challenges/1)

##### :sunglasses: Markdown :cool:

Want any text you have on Github to look :fire: hip and trendy :tada:? Learn how to write [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and use [Emojis](https://www.webpagefx.com/tools/emoji-cheat-sheet/) in the markdown is a great way to get started :100: :thumbsup: :ok:

### Resources

- Google Chrome
- Atom / Sublime
- VS Code / JetBrains
- Plugins
- React
- Firebase
- MDN
- `npm`
  - how to install modules and stuff
- webpack & build tools
- automated testing

### Tools

idk this is kind of links resources too, just braindumping at the moment

### Keyboard Shortcuts

- CLI
  - `.bashrc` aliases and creating your own
  - `ctrl + c` to clear the line
  - hitting up to go through the cli history
  - Link to CLI / bash shortcuts
  - `git`
    - all things `git` students will most likely use

- Github
  - `t` in Github
  - `b` for Zenhub if setup

- Google Chrome
  - `ctrl + shift + i` / `cmd + shift + i` to pop the Developers Console
  - `ctrl + shift + c` / `cmd + shift + c` to Inspect Elements & Pop developer's console
  - `ctrl + shift + r` / `cmd + shift + r` to hard refresh the browser and clear cache
  - disabling cache
  - changing developer's consolve to Dark Theme
  - and youtube while you're at it tbh




  Made with :heart: by some nerd in Seattle
