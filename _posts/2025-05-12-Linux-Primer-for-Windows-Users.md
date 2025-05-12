---
title: A Practical Guide to Linux for Beginners
date: 2025-05-12 16:51:00 -0400
category: [articles]
tags: [linux, guides]
description: Things nobody will tell you about Linux when you're just getting started as a Windows user
published: false
---

Whether you can't or won't run Windows 11 and looking for alternatives with Microsoft [ending support for Windows 10](https://www.microsoft.com/en-gb/windows/end-of-support) later this year, ready to embrace the Year of the Linux Desktop, or simply looking to expand your horizons, there has never been a better time to make the switch to Linux. Linux still seems to carry the stigma of something that is relegated strictly to the realm of basement-dwelling nerds - difficult to understand, even more to difficult to use, no driver support for modern hardware, a buggy mess which requires extensive knowledge of the command line interface in order to accomplish simple tasks, etc. But many of these points, which were absolutely well-deserved criticisms in 2005, are no longer true 20 years later.

Mature distributions like Ubuntu or some of its popular cousins like Linux Mint are entirely capable of providing a grandma-proof desktop experience in 2025 - that is, for the average person's use case (mainly the ability to open a web browser in order to access email, youtube, shopping, social media, etc.) it is easier than ever to install and use Linux as a daily driver without ever touching the command line or having to know much of anything about how computers work. Valve has even made massive strides in recent years in bringing gaming to Linux with [Proton](https://en.wikipedia.org/wiki/Proton_(software)) and [SteamOS](https://store.steampowered.com/steamos/) which powers their Steam Deck.

That being said, much of the beauty of Linux comes from the power and freedom of choice the command line gives you, and if you're just getting started with trying to learn Linux for work or school purposes, you're probably looking for a bit more information than how to open the browser.

## The Current State of Things
---

Nearly every "getting started" guide for Linux out there goes something like this:

  - Some obscure discussion about kernels, terminal emulators, release schedules, and other cryptic information that probably doesn't mean anything to you at this point
  - How to choose the right distribution based on the previous discussion
  - How to install it
  - A list of 50 million commands you should start typing immediately
  - Consult the manual if you have problems

And then of course if you try to ask questions, you are almost guaranteed to get this response:

![rtfm.jpg](/assets/img/linux-primer-for-windows-users/noob.jpeg)
_A wild Arch Linux user in his natural habitat_

I'm not going to make any attempt to sway you towards any particular distribution or turn you into a professional command-line ninja in this article. There is no shortage of excellent reference material out there when it comes to these points above, but it seems some crucial context for really and truly *getting started with Linux* is always missing:

  - Why are there so many options?
  - Why can't I install any programs?
  - How do I *do stuff*?

This more or less sums up the new operating system vertigo I still remember feeling when I was first getting started. Linux is more than just a new set of desktop wallpapers and buttons, it's a completely different way of thinking about what a computer is and how it should be used, which will more than likely require a bit of "un-learning" of the habits you developed when learning to use Windows. Hopefully once you find yourself staring at a freshly installed Linux desktop, you will be able to find answers to these most burning questions (or at the very least be able to form the basis of more specific questions) right away with the information presented here. 

## The Anatomy of a Linux Distribution (or "distro")
---

So what exactly is a distro and why do you have to choose one? The thing is, Linux is really more of an idea than an operating system. I won't get too deep into the open-source philosophy of Linux here, but I will make some rather large oversimplifications of it for the sake of understanding it (I promise this will be relevant shortly!)

Imagine that Microsoft is a car manufacturer instead of a tech company. They only produce one car model that anybody cares about, as well as all of the parts required to build it, and it's called Windows. Every few years this model gets a facelift and maybe some new bells and whistles, but you more or less know what you're going to get - a car with 4 wheels that works most of the time (hopefully). Linux, on the other hand, is just an engine, and a "Linux Distro" is an attempt to build a functioning car around that engine by attaching other useful components like a transmission, tires, seats, and so on and so forth. Unlike Windows, which comes complete with every part of the car being crafted by Microsoft, Linux is just what powers the car, and all the components are produced in a massively decentralized fashion by independent contributors with (generally) no affiliation to any corporate or government entity.

The nice thing about this decentralized production scheme is that all the components are built from the ground up with the idea that A) a component should do only one thing and do it well, and B) it should be easy to swap or modify that component later, because the blueprints for not just the overall car, but also all of its individual parts are available to anyone that wants them. So if you don't like something about your car, you can simply remove that thing and replace it with a different one made by somebody else - or you can even make your own! Maybe you want a car with 3 wheels, or 28 wheels, or maybe you also want your car to be a boat; knock yourself out. Windows is almost the exact opposite of this. You cannot see the blueprints (closed-source), which means no one other than Microsoft can deeply understand how everything works behind the scenes, and as such, you more or less cannot make any modifications that Microsoft doesn't want you to make.

![Linux HQ](/assets/img/linux-primer-for-windows-users/hq.jpg)
_Fun fact: The internet as we know it would probably cease to exist if it weren't for some dude named Jeff thanklessly coding in his spare time_

Now, there are a *metric shit-ton* (that's 2.55 standard shit-tons) of components required to build a car, and likewise probably even more software components that make up a Linux distro, but for the quick-and-dirty beginner's guide I propose that there are really only 2 main software components worth thinking about, which comprise every modern distro (and also the main immediately observable differences between Linux and Windows):

  - A **desktop environment** (that is, the "GUI")
  - A **package manager**

Here someone who is not a beginner might ask questions like "what about init systems? what about file systems? what about the windowing system? what about the shell? what about the network stack? what about the bootloader? what about the maintainers deciding to do XYZ differently from upstream? what about..." and to those people I say, this article is not for you 😎 Now let's review these 2 major components:

### Desktop Environments (DE)
This is almost certainly an unpopular opinion among Linux people, but it is mine nevertheless: the DE is probably the most important part of choosing a distro for beginners, because if you find the user interface is frustrating to use and you can't use your computer to do computer things at all, you probably will have a hard time finding the motivation to learn how to do things in the terminal. Learning a new desktop environment is also going to be challenging at first, but much less so than the terminal if you have never used it before. Personally I prefer breaking big tasks into smaller, more easily achievable wins rather than trying to do everything all at once - start with the easy thing before moving on to the hard thing.

> If you don't want to think hard about choosing a DE and would prefer to skip this section, my tl;dr opinion for Windows users would be to start with a distro that has a KDE option and see where that takes you.
{: .prompt-tip }

There are probably hundreds of options here, and lately it seems that it is becoming more common to see that a single distro will come with several different installer options that allow you to choose the DE you want up front, so it is worth having at least a general idea of some of the choices you might see. Without getting too far into the anatomy of a desktop environment, there are again really only 2 main DEs to be aware of, and then some (more or less) popular offshoots of those:

#### KDE Plasma
Based on the Qt toolkit, this provides a feature-rich, highly customizable interface that will feel immediately familiar to Windows users. Honestly this is probably the best place to start if you feel overwhelmed by the sheer number of DE choices out there, because you can change pretty much everything about it to look and behave exactly the way you want. Some other notable members of the Qt family:

  - **LXQt**: more or less a stripped down minimalist version of KDE that works well on older hardware
  - **Trinity**: a fork of the older KDE 3.5 which aims to preserve this experience, maybe a good choice if you yearn for the glory days of Windows XP

#### GNOME
Based on the GTk toolkit, this is a popular yet polarizing choice and the default for many mainstream distros such as Ubuntu and Fedora. It provides (compared to KDE) a somewhat minimal experience: by default there is no system tray, no task bar, and there are no desktop icons or widgets. Customization options are limited and many things you would normally do with a mouse are more easily done with keyboard shortcuts, but this allows for a pleasantly clean and simple look that doesn't distract you from your work while still being powerful enough to do most of what you need a DE to do. This is my personal favorite so far, but there are quite a few other options based on GTk if the highly opinionated decisions of the GNOME developers rub you the wrong way:

  - **MATE**: aims to preserve the design philosophy of GNOME 2, generally a simple and lightweight experience
  - **Cinnamon**: aims to preserve the design philosophy of GNOME 3 (remember when I said GNOME was polarizing?), now a heavier and feature-rich experience similar to Windows
  - **Budgie**: a heavier and more customizable "traditional" desktop experience, not a fork of any particular GNOME version but heavily relies on some of the underlying apps and components
  
#### "Others"
Also GTk-based but started as independent projects completely separate from GNOME, these show up frequently in any DE discussion:
  - **LXDE**: the spiritual predecessor of LXQt, which is the Qt rewrite of LXDE. A lightweight choice for older hardware
  - **XFCE**: probably the most popular truly lightweight, minimal DE which is also a good choice for old or low power hardware

> The choice of Qt or GTk is almost entirely insignificant, as apps built with either toolset will still work on "the other" DE. You don't need to bother with understanding the difference between the two, it is only mentioned here because apps from a given toolset tend to be somewhat constrained to a certain kind of look and feel.
> 
> In the event you find yourself wondering why a specific app looks weird, doesn't match the rest of your desktop theme (or rarely, has a bug that affects functionality), there's a good chance it has something to do with these underlying components, so it's good to know which components you're trying to use.
{: .prompt-info }

##### Window Managers (WM)
It's also worth briefly mentioning here that every DE uses a Window Manager, and hopefully this is not a surprise at this point, but the WM can also be changed. It's also possible to use just a WM without any DE at all, although this is considered a setup for advanced users. This allows you to see and arrange the GUI windows that an app displays, but otherwise does not have any of the components of a "Desktop" that you would expect like a clock, file manager, a utility to change system settings, etc. Using just a WM gives you essentially a hybrid command-line-only system which can also display limited graphic elements like a browser window or a code editor. Just know that if you come across this term, what you are looking for as a beginner is a Desktop Environment, *not* a Window Manager.

### Package Managers
Package managers are a significant departure from the way things work in Windows, and there is one at the heart of every distro. In a nutshell, a package manager is like the app store in android or iOS devices, and much like the way you download apps from the app store on your phone, with Linux you download the programs you want to use from the package manager. If you really sit down and think about it, the way you install new programs in Windows is kind of weird and crappy - you google the name of a program and start clicking around on random websites trying to find a link to what you want, and often there are ads disguised as download links for the thing you're looking for, or even worse, the link is a malware installer. Once you finally get the real installer for the program you want, you need to click through a bunch of menus to uncheck all the options to: sell your personal information to third parties; sign up for email lists; install browser plugins or God knows what else; and if you're really unlucky, once you have done all that you will be rewarded with even more ads. In many cases you also still have to pay for the privilege of sitting through this ordeal in order to get a license to activate the features of the software you really wanted to use in the first place.

![Microsoft](/assets/img/linux-primer-for-windows-users/microsoft.jpg)
_I'll blame anyone as long as it's not me_

This is where that open source philosophy I mentioned earlier comes into play. Linux has none of these problems - you can essentially open a terminal, type in a command resembling "download my-desired-program" and... begin using your program a few seconds later. That's it. Everything is free (and ad-free) and the repository of software you can download is curated by the distro maintainers, so you can be sure you're downloading exactly what you think you're downloading. You don't need to download a .NET framework or C++ redistributables or try to figure out why some random .dll file is missing, because the package manager ensures all the components required to run a program are *also installed* alongside it. Furthermore, the source code of everything you can download is open for inspection by anyone, so you can really be 100% sure that apps don't come with any hidden malicious behavior (and even if you personally are not reviewing the code, rest assured that thousands of nerds around the globe are).

Many distros now even provide a sort of GUI app which allows you to install apps just by clicking, much like any other app store, although these tend to be quite limited in my experience and you are going to end up needing terminal commands regardless if you really want to do *work* that can't be done in a browser. And while in most cases everything you need will be in the package manager, it IS still possible to download and install software "from random websites" in Linux, but that generally must be done in the terminal, and it requires a bit of understanding about how your package manager works (unless you want to get into building software directly from the source, which is another story for another time).

In order to find the right commands, you first need to know which package manager you're using. Unlike desktop environments, it's almost always possible to tell which package manager you're using just by knowing which distro you're using. Much of the philosophy of a distro manifests itself through the package manager, in the form of the distro maintainers deciding (or not deciding) which packages are available there and how frequently they are updated. This is to say, it would generally be *really difficult* (although not entirely impossible!) to switch from one package manager to another within the same distro because of how much the underlying operating system relies on the package management system.

With all that being said, the most common package managers and their associated package formats are listed below. Note that in all of these cases, the name of the package manager is also the name of the command used to run it - how convenient!

  - **apt** (Advanced Package Tool)
    - uses the ".deb" package format
    - uses the `dpkg` command behind the scenes to perform low-level interactions with .deb files
    - used by Debian and most of its derivatives (Ubuntu, Linux Mint, Pop!_OS, Kali Linux, Raspberry Pi OS, and many more)
  - **dnf** ("DaNdiFied yum") or **yum** ("Yellowdog Update Manager", old version but interchangeable with dnf)
    - uses the ".rpm" package format
    - also uses the command `rpm` behind the scenes to perform low-level interactions with .rpm files
    - used by CentOS Stream, Fedora, Red Hat Enterprise Linux, Rocky Linux and others; common in enterprise server environments
  - **pacman** (hopefully the naming convention here is self-explanatory)
    - generally uses ".pkg.tar.zst" format, although you may see other ".pkg.tar.*" formats
    - `pacman` does not have a lower level helper command - one command does it all!
    - used by Arch Linux and its derivatives (Endeavour OS, Garuda Linux, Manjaro, SteamOS, and many more)
  - honorable mention: **zypper**
    - used exclusively by openSUSE and SUSE Linux Enterprise
    - also uses `rpm` and .rpm files like dnf/yum, but zypper/SUSE .rpm packages are most likely NOT interchangeable with dnf .rpm packages - be careful!

Notice that it seems to be a common practice to have both a higher level interface (like `apt`) and a lower level interface (like `dpkg`) for working with packages. You could think of this sort of like a vending machine: what you really want is a coke, so you press the coke button, and a coke comes out. This is what `apt` handles for you, it's presenting the menu of buttons which can be pressed. Behind the scenes, `dpkg` is the program controlling which motors inside the vending machine need to turn and how far or for how long each one needs to turn in order to put your desired product in your hand. You could eventually figure out how to get the same result as pressing the coke button on the outside using this low level program, but it's much nicer to just press one button when there's no need to specify all the gritty details. So, in most cases you will use the high level interface to do stuff, but it's worth being aware of this association here because it's also not uncommon to see tutorials out there which use the low level commands instead.

You might also come across mentions of things like Snap, Flatpak, or AppImage - these are all attempts at self-contained app "sandbox" environments which bypass package managers entirely by including all the required dependencies in a single package, which in theory means that the exact same version of an app can be installed in *any* distro regardless of the package manager or environment-specific unknowns. In theory a great idea, but in practice there are downsides to this approach as well, namely that there will be some additional storage space and/or CPU overhead required to run these apps. There is a time and place for everything and I would say the best use of these formats is to install something not provided natively by your package manager - otherwise, you are probably better off at least making an attempt to get the native version working first.

## The Foundation of Doing Stuff
---
Now that you've seen some of the big ideas that differentiate Linux distros from each other, let's look at some concepts that are generally the same in every distro (but very different from Windows) which are really crucial to developing the fundamental understanding of why things are the way they are in Linux and how to navigate around them.

### Filesystem Roots and Paths
In Windows the storage space on your computer is organized by "drive letters" accessible from My Computer - typically the operating system and all your programs will be installed on the C drive, and any additional drives (hard drives, USB flash drives, SD cards, CD/DVD drives, network attached storage, etc.) will have an additional drive letter from D to Z. And a fun fact for anyone born in this century: drives A and B were historically reserved for floppy drives, which is why your hard drive always starts at the letter C and not A.

The drive letters act as the "root" of each drive, the highest organizational level at which files and folders can be created. File paths always start with the root, for example `C:\`, and below that you have files or folders for organizing stuff: `C:\Program Files` for your installed programs, `C:\Windows` for operating system files, etc.

In Linux, there is no such concept of drive letters. Instead, there is *only one* logical root for the entire system, which begins at the top-level path `/` (notice the path separator in Linux is '/' and '\\' in Windows) and is not strictly associated with any physical device. This begins to make much more sense in the context of servers and supercomputers, where you may not only have hundreds of drives, you may also have hundreds of separate computers that are connected to each other, acting as one big computer and sharing those drive clusters. In this case you would find yourself quickly running out of letters, and not wanting to think about which physical drive or machine a file is associated with. Also, everything else (not just drives, but *all* hardware connected to your computer) is represented as a file somewhere under this root. More on that in just a second, but first some additional noteworthy differences:

  - Paths are case sensitive in Linux (you can have 2 different folders called downloads and Downloads) while in Windows they are not (downloads and Downloads are the same folder)
  - Windows paths and filenames often contain spaces. Linux filenames *can* contain spaces but this is inconvenient and frowned upon since the space character is also used to separate command line arguments
  - Windows paths and filenames cannot contain many special characters such as `<>:"\/|?*`. In Linux you can name files with almost any character other than an unescaped `/`, even UTF-8 characters like emojis
  - File extensions like .exe or .txt are important in Windows. In Linux the file extension has less significance and is not necessary at all, but they are still often used as a hint to what the file contains or which program should be used to open it
  - Some applications may have trouble with path names longer than 260 characters in Windows, in Linux this limit is more easily configurable and often set to 4096 by default
  - Windows has "shortcuts", most commonly on the desktop, which are a specific type of file (.lnk) that can open the location of another file. Linux has the roughly equivalent concept of "symbolic links" or more commonly "symlink" at the command line level which creates an alias or pointer from one file path to another

You will probably also notice that the top-level folders in a Linux system have cryptic names like `/bin`, `/etc`, `/mnt` rather than human-readable ones like `C:\Program Files`, `C:\Users`, `C:\Windows`, etc. But there is a method to this madness called the [Filesystem Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard) which describes what you should expect to find in each of these folders.

### Everything is a File
Absolutely everything in and around your computer is represented as a file somewhere in the filesystem in Linux. Folders are files. System settings are files. Network interfaces are files. Processes are files. Even your CPU, monitor, and keyboard, believe it or not, also files. The "everything is a file" philosophy takes some getting used to, and in fact it also explains a lot about why Linux is (or more recently, was) so heavily reliant on the command-line. When everything is a file, it's very easy to represent everything (data, resources, commands, etc.) as a text stream. By abstracting everything to file operations, there is only one standard set of tools and a single interface through which pretty much everything in the operating system is accomplished. For example, the output of some program which was supposed to be displayed on the screen could instead be just as easily saved in a file on your hard drive, or sent to another device across the network. That's possible because your screen, hard drive, and network are all just files which use the exact same input and output system, and it's trivial to choose *which* file a program will output to.

![everything is a file](/assets/img/linux-primer-for-windows-users/files.jpg)
_Memes are files too_

In Windows the idea is "everything is an object". Every object type has essentially its own API that the operating system can use to interact with that object, and you interact with this object indirectly by obtaining a "handle" or reference to that object through the API. This model lends itself well to graphical user interfaces, because a text-based interface becomes significantly more complicated when screens, hard drives, network interfaces, etc. all use a different interface and can't interact with each other directly or share a common toolset. Essentially Windows started as a powerful GUI which had a command-line interface bolted to it later, while Linux started as a powerful command-line interface which had a GUI bolted on later.

### Ownership and Permissions
Linux has a relatively simple file permission system, although the much more sophisticated Windows permission system rarely needs to be touched by anyone outside of a corporate IT department, so there is a good chance you have never given much thought to this topic anyway. I won't explain it in great detail here, but would highly recommend looking to something like the [Red Hat Blog](https://www.redhat.com/en/blog/linux-file-permissions-explained) for an in-depth explanation of how to interact with the file permission system in Linux because it is an important topic. But for the short and sweet version, there are essentially three ownership classes in Linux:

  - **User** (that's you)
  - **Group**, a named list of one or more users
  - **Everyone**, that is, any user anywhere who is not explicitly mentioned by a user or group ownership definition

Every file is considered to be owned by 1 user (usually the creator of the file) and 1 group, effectively granting the ability to extend ownership to multiple users if necessary. Each ownership class also has 3 permission attributes which can be set independently:

  - Read
  - Write
  - Execute

These are exactly what they say they are: the ability to read the file contents, the ability to write or modify the file contents, and the ability to execute the file contents as a script. The 3 groups and 3 permissions can be used in any combination, so for example a file containing some program could have the full permissions read, write, execute for the *user* that owns the file, while any users belonging to the *group* that owns the file could be limited to only reading or executing the file, and finally *everyone else* can be restricted to only executing the file, without being able to read it or change it in any way. While there are special extended permission attributes and things like Access Control Lists that allow for more granular control of who can do what with which files in enterprise environments, these are far beyond the scope of this article.

If you find yourself wondering *Why does it matter? Why do I need to know this?* consider that the Linux file permission system is a remnant of the time before personal computers were really a thing. Before the PC - a time long before I was born that I have only heard about through my parents - there were "mainframes" (servers) and "terminals" (clients), basically just one big computer that everyone in a university or office building shared through the use of distributed terminals, which in turn were little more than a screen and keyboard with long cables that provided a means of interacting with the mainframe. Today Linux still operates on the assumption that the computer is a *server* (which quite frankly is still a very common use case, see *the internet*) which will be accessed by multiple users simultaneously. So the ability to control file access at the individual user level is much more important than it is in Windows, which is primarily built around the assumption that everyone will have their own separate computer and nobody will ever have a reason to connect directly to yours.

>File permissions only apply while on the computer that holds the file - if you transfer the file to another computer, then the owner of that machine will be able to change the owner and permissions as they see fit, so these permissions *do not* necessarily prevent people from stealing your files and doing whatever they want with them
{: .prompt-info }

A noteworthy caveat to this permission system is the *super user*, which is for all intents and purposes equivalent to the "Administrator" in Windows, just a much more extreme version. The super user is granted all permissions on all files, which is equal parts terrifying and dangerous. There is a joke commonly posted online which goes something like "to save hard drive space after installing Linux, make sure you delete the French language pack with this command:"

> **Do not do this**
> 
> `$ sudo rm -fr /`
{: .prompt-danger }

Probably sounds like reasonable advice to the uninitiated, but this will irreversibly delete *everything* on your hard drive, including the operating system. So in short, don't run commands you don't understand - with great power comes great responsibility.

Finally, no Linux primer would be complete without mentiong the `sudo` command - I guess I sort of already did, but this is short for "super user do" and gives the subsequent command the ability to run as the super user, which means it will ignore all permission and ownership settings. Prefixing a command with sudo is roughly equivalent to "Right click -> Run As Administrator" in windows, or bypassing the User Account Control popup that asks if you're *really sure* you want to allow this program to make changes to your computer. Really, it's more like releasing the safety from a gun and pulling the trigger, so again, *pay attention* when running any commands that start with sudo.

### Command Line 101
Last but not least, let's just call it like it is because there is really no other way around it: becoming proficient in the use of a Linux shell is a somewhat difficult and probably painful process that is going to require a good bit of dedication and patience on your part. For lack of better words, it requires a lot of ass-in-seat time to develop the muscle memory required to be able to get anything done without having to look up how to do it every time. Ubuntu provides [an excellent tutorial](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview) for getting started with the basics of this process. But there are still a few points every guide seems to miss, which in my opinion would have been nice to know in the beginning rather than sporadic 'aha' moments popping up months or years later.

#### • Terminals vs Shells
The terms terminal and shell are often used interchageably, and I'm not here to rain on your parade and say that you can't interchange them, but there is actually a difference between the two which is important to understand if you ever want to (or have to) use a different version of one or the other. One would imagine this should be a question that is easy to answer in plain english, but the top Google results for any variation of "terminal vs shell" seem to provide information which is at best overly pedantic or difficult to understand and at worst just downright incorrect. So I'll try to lay it out in just one sentence to set the record straight: A **terminal** is a GUI application (think VScode, Visual Studio, insert JetBrains IDE of choice) which provides access to a shell, and a **shell** is a text-based program which provides an interface to the operating system (think interpreted languages like Java or Python).

To put that another way - the terminal is the name of the program that will be displayed on the screen (such as `konsole` if you are using KDE, or `gnome-terminal` if you are using GNOME) and the shell (most commonly `bash`, could also be `fish`, `ksh`, `tcsh`, `zsh`, etc.) is the name of the command interpreter and scripting language that determine which commands you are able to write.

The pedantically correct term is 'terminal emulator' because a 'terminal' as mentioned earlier is a hardware device and not an application, but hear me out: *Life is too short for this argument and nobody cares*, just say terminal.

#### • Don't copy the dollar signs
Thankfully this seems to be dying out, but it's still not uncommon to find shell commands written in tutorials and forum posts like this:

```bash
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install package1 package2
```

The **$** is not part of the command and this is often not immediately obvious to new users copy and pasting stuff from the internet. This is, however, actually an important signal that you should be running these commands as a normal user and not the super user, as that's typically what you see when opening a terminal:

![Human User](/assets/img/linux-primer-for-windows-users/terminal1.png)

You might also see the commands written like this instead:

```bash
# apt update
# apt upgrade
# apt install package1 package2
```

Notice the **#** instead of **$** - this means the command should be run *as the super user*, which means you probably need to add `sudo` to the front unless this is going to part of a script which will be run with sudo later. An example as the super user, which you can see begins the command prompt with **#** instead:

![Human User](/assets/img/linux-primer-for-windows-users/terminal2.png)

#### • RTFM
Unfortunately, reading is an unescapable fact of life when it comes to learning Linux, and you will be doing a lot of it. Fortunately most of it is already built into the operating system and doesn't require internet access. Any time you find yourself copy and pasting commands from somewhere and don't know what you're looking at, it's generally good practice to spend a few minutes reading the *man page* first (that's man as in manual, not men, but it will still be hilarious at some point in the future) to try and get an idea of how the person or LLM who wrote the command was able to come up with it in the first place. You can also generally always type `<command> --help` to get syntax hints and a short summary of available options, while the man page provides all the gory details. There is a man page for the shell you're using, so assuming you're using `bash`, you can simply type:

```bash
man bash
```

to view the manual for bash itself. There is even a man page for the man command, so `man man` is the one man page to rule them all. If `man` isn't installed by default it's usually at least available from the package manager.

The bash manual is quite long and dense, and to be honest I have not read most of it because I learned a lot of it "the hard way" before ChatGPT was a thing - by scouring stack overflow posts for the meaning of commands I found in other stack overflow posts. Looking back, I could have saved a lot of time by learning how to read the manuals instead, basically cutting out the middle men and going straight to the source of truth rather than having it filtered through the minds of people who may or may not have any idea what they're doing. But anyway, the bash man page does explain in great detail the answer to almost any kind of "how/why did they do that?" question you could have when coming across bash commands in the wild. There are also quite a few gems to be found in there if you're willing to attempt it as a beginner, namely:

```bash
compgen -b
```

This command will provide a list of every command which is built into bash itself (that is, not commands which are part of the operating system or its installed programs, but the commands that will always work in any distro anywhere you find a bash prompt). Many of the same commands will be available in shells other than bash, which is to say, reading the man pages for the commands in this list will give you a really solid understanding of what you can do in a terminal, a level of understanding that will likely even transfer outside of Linux to other Unix-like environments such as Android and Mac OS.

If you sit down in front of any random Unix-like device and don't even know what shell you are in, you can also generally do this to find out:

```bash
echo $0
```

#### • Text Editors and Keyboard shortcuts
The familiar ctrl-C / ctrl-V, ctrl-f, and ctrl-z from Windows generally don't apply to anything you will do in the terminal. Any time you need to edit system configuration files, you generally need to open them using a command like `sudo <text-editor> <file-path>` because clicking on files in the file explorer will open them with something like `kate` in KDE or `gnome-text-editor` in GNOME as your regular user, which means you won't have permission to save the file. You can just add `sudo` to your GUI text editor command, but if you need to do something on a headless or remote system and it's not possible to use the GUI app it's good to know how to do this the old fashioned way. There is an easy-to-use terminal text editor called `nano` which is available from every major package manager and installed on most systems these days by default. Many people will tell you to learn the more powerful (and also more difficult, at first) `vi` or `vim` because it's going to be available on basically everything ever built since the '70s, or that you need to learn `emacs` which is almost a second operating system that turns your terminal into a GUI app where you can't use the mouse - that's up to you, personally I think if you can't do something in `nano` it's time to open a VScode remote session and save the brain space that would be used for all those keyboard shortcuts for something more important.

`nano` is kind enough to show you some commonly used keyboard shortcuts are every time you open a file (note that the bigger the window gets, the more shortcuts that will be displayed):

![nano](/assets/img/linux-primer-for-windows-users/nano.png)

Although at first glance this probably doesn't mean anything to you, the short and sweet version is that `^` stands for ctrl
