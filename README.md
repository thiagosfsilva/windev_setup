# Setting up a geospatialanalysis and development environment on Windows
 
## 0) Enable dark mode

No, seriously, it looks so much better and gives you a lot less eye strain. Right click on your desktop, choose `Personalize` and then on the `Colors` tab, select `Dark` under `Choose your color`. Boom, now you're a dev.
 
## 1) Install Windows Terminal from the Microsoft Store
 
 If you're serious about data science and/or development, you can't stay away from the terminal forever. Not having a decent terminal was a Windows drawback for years, but now we finally have a pretyy decent one! Just head to the Microsoft Store and search for Windows Terminal. You can install the regular version, or the Preview version if you want to be at the bleeding edge. Just maker sure it is the offcial one made by Microsoft, there is a lot of crap there trying to trick people. 
 
## 2) Install Chocolatey and/or WinGet for package management
 
 The second major limitation of Windows against Linux and Macs was the lack of a package management system. Every Linux distribution has one (apt, rpm, pacman, etc.), and Mac has had the unnoifical HomeBrew package manager for years. Chocolatey is the equivalent of Homebrew for Windows, and recently Microsoft has phagocited Winget, making it the "official" Windows package manager. I currenlty use both but prefer Chocolatey as it is older and more stable, and because of the [controversial back history](https://medium.com/@keivan/the-day-appget-died-e9a5c96c8b22) of Winget.
 
Follow the instructions to install [here](https://chocolatey.org/install). An **administrative shell** means you open *Windows Powershell* as administrator. Chocolatey is a command line (i.e. terminal based) application, but there is also a graphical user interface (GUI). I've never used the GUI, but conveniently, you can install it using choco itself. 

Once you have choco installed, you can search for a particular program in the terminal by typing `choco search nameofprogram`. You can then install is with `choco install nameofprogram`. You can then update a single program by using `choco upgrade nameofprogram` , or update all programs installed by Chocolatey with a simple `choco upgrade all`. Oh glory!

Except for searching, these operations need adminstrator priviledges too, which brings us to…

## 3) Install *gsudo*

Have you ever seen Linux and Mac users throwing *sudo* jokes around and felt left out? Worry not! Sudo, which means *super user do* is the equivalent of *Run as Admnistrator*, but it works from the terminal, and only applies to the specific command that is appended to:

![Obligatory xkcd cartoon](https://imgs.xkcd.com/comics/sandwich.png)

It is extremely convenient, because you don't need to remember to start your terminal in admin mode, then do what you need to do, and then close it because you don't to do everything as admin (unnecessary security risk). Install it using `choco install gsudo` (this is the last time you' ll have to explcitly open your terminal as administrator) and rejoice. From now on, every time you need to do something that requires admin privileges, you can just type `sudo` before the actual command. It will still open a Windows UAC window for you to accept, because well, it's Windows...but already a lot better than right-clicking. 

##  4) Install some key apps

Other key apps you will need to develop on windows are a good text editor and a good IDE. My suggestion is to use Notepad++ for text and Visual Studio Code for IDE. Yes, technically they are both text editors, and both can be used as IDEs, but in practice I find Npp (as Notepad ++ is charmingly referred to) to excel at zero-delay opening and editing simple text files, while VSCode will give you all the bells and whistles of a full IDE (via extensions). I specially like that Npp adds a context menu entry, so you can open any file in it with a right click + choose `Edit with Notepad++...`. And I mean ANY file. 

I also recommend installing 7-zip, to me it is the best file compression/extraction tool for Windows, and it will decompress anything you throw at it. Some people swear by PeaZip instead. 

Finally install Git. If you are serious about becoming a data analystor developer, version control is a requirement, and pretty much everyone uses Git for that. No, Git is not the same thing as GitHub (we' ll ge there). 

You can install them all using...choco! ` sudo choco install 7zip vscode notepadplusplus git ` and Bob's you're uncle.



