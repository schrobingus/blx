# Blocks Package Manager
Blocks, or known in the command line as "blx" is an adaptable and centric package manager built for Modulus Linux written in POSIX shell. It's aim is to be as flexable and minimal as possible, while still giving the user control over everything.



## Installing
(At the moment, Blocks is very experimental, and should not be used as a daily package manager until stable.)
1. Download the blx script, or clone the repository.
2. Copy the script to your binary directory. Usually is `/bin` or `/usr/bin`.
3. Mark the script as executable so it can be ran.
4. As superuser, run `blx setup` to set up the directory structure and Modulus repositories.



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
- KISS has decentralized and decentralized repository structure that aims at making a repository as easy as cake. Blocks can also have external repositories, but it isn't it's main priority.
- Blocks is built to use the main repositories primarily (but can be used with external ones), and there's no specific direction of how packages are supposed to be (the exception here being if they're binary and or proprietary, which might get it's own mini-repository).
- Because KISS has decentralized and customizable repositories, that means less sphagetti code, and more freedom from developers, which ensures that a ton of maintained repositories will contain installable software.
- However, if a single maintainer goes dormant on a KISS repository and new software is released, the software will not be updated, it just becomes more outdated over time. The Blocks repositories will orphan packages if the maintainer goes dormant, and will hand them to a new and willing maintainer to keep them up to date.
- At the moment, while Blocks is unstable and in heavy development, it seems to be pointing that it will have less lines of code than KISS (predicting around 500 lines compared to KISS' 2000), however, Blocks packages are not temporary, which will take more and more disk space unless you manually clean out each package.
