# Blocks Package Manager
Blocks, or known in the command line as "blx" is an adaptable and monolithic package manager built for Modulus Linux written in POSIX shell. It's aim is to be as flexable and minimal as possible, while still giving the user control over everything.



## Installing
Blocks is in a very unusable state at the moment that is specific to my current setup (and the Modulus file structure), but this will eventually change. For now, if you want to test it, I'd highly advise doing it in a VM as this is currently experimental software. 

To install, just simply copy the blx script into the /usr/bin directory (and mark it as executable).



## Features
- Easy to understand package structure.
- Managed by short POSIX scripts.
- Linking external packages and their source directly to their location.
- Ease of modification, making processes like patching easier.
- Ability to ban packages from getting installed.
- Banning packages also applies to dependencies.
- Manage, add, and remove features with ease as it doesn't have to be compiled.
- Only dependency is a reliable set of UNIX core utilities.



## Blocks vs KISS
Blocks is heavily inspired by the KISS package manager, but there are quite a few differences to mention, both pros and cons of each.
- KISS manages the source of packages temporarily, and only keeps the tarball or Git repository referenced. Blocks keeps the source where the package is, whether you use it from the repositories, or use an external package.
- If an unneeded dependency is referenced, it can simply be removed from KISS and Blocks. If it keeps popping up, you can ban the package with Blocks.
- KISS has decentralized and non-monolithic repository structure that aims at making a repository as easy as cake. Blocks can also have external repositories, but it isn't it's main priority.
- Blocks is built to use the main repositories primarily (but can be used with external ones), and there's no specific direction of how packages are supposed to be (the exception here being if they're binary and or proprietary, which might get it's own mini-repository).
- Because KISS has decentralized and customizable repositories, that means less sphagetti code, and more freedom from developers, which ensures that a ton of maintained repositories will contain installable software.
- However, if a single maintainer goes dormant on a KISS repository and new software is released, the software will not be updated, it just becomes more outdated over time. The Blocks repositories will orphan packages if the maintainer goes dormant, and will hand them to a new and willing maintainer to keep them up to date.
- At the moment, while Blocks is unstable and in heavy development, it seems to be pointing that it will have less lines of code than KISS (predicting around 500 lines compared to KISS' 900), however, Blocks packages are not temporary, which will take more and more disk space unless you manually clean out each package.
