# Blocks Package Manager
Blocks, or `blx` is an experimental and adaptive package manager for Linux written in pure POSIX shell. It's designed to use a centralized repository, but is extremely flexible in the way you'd like with several organization features. Note that it is very incomplete and should not be used for a system.

## Installing
Download the shell script, mark it executable, and run `blx setup` as root. This can be summed up in one command that needs to be run as a superuser with wget: 

`wget https://raw.githubusercontent.com/moduluslinux/blx/master/blx -O /bin/blx && chmod +x /bin/blx && /bin/blx setup`

## Features
- Easy to understand package structure.
- Managed by short POSIX scripts.
- Linking external packages and their source directly to their location.
- Ease of modification, making processes like patching easier.
- Ability to ban packages from getting installed.
- Banning packages also applies to dependencies.
- Manage, add, and remove features with ease as it doesn't have to be compiled.
- Only dependency is a reliable set of UNIX core utilities.
