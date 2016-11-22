# WHAT IS DOCFILES
## Introduction
   * Dotfiles are used to customize system
   * It can help us to automate all the things

## Some important dotfiles
   * *.bash_profile*: This file in home directory is loaded first. Some people like to put most of their startup configuration in one file.
   * *.inputrc*: Store all behaviors of line input editing and keybindings.
   * *.alias*: Allow to define shortcuts for commands, to add default arguments, and/or to abbreviate longer one-liners.
   * *.fucntion*: Commands that are too complex for an alias can be defined in a function
   * *.env*: Environment variables can go in another dotfile.
   * *.prompt*: There's plenty of options, that can show where you are in the directory tree.

## Get started
   * Need to organize it as a USB drive. Store it in a version control is great e.g GitHub.
   * Include all files in a folder (e.g /Users/lars/Projects/.dotfiles), then run:
   ```
   for DOTFILE in `find /Users/lars/Projects/.dotfiles`
   do
    [ -f “$DOTFILE” ] && source “$DOTFILE”
   done
   ```

# INSTALL
1. Create new folder *dotfiles*: `mkdir dotfiles`
2. `cd dotfiles/`
3. Clone code from: git@github.com:ningo-asnet/dotfiles.git
4. Then link files from cloned folder to home: 
*OSX*
(E.g link to `.bash_profile`)
```
ln -sv “~/dotfiles/.bash_profile” ~
```

*Ubuntu*
(E.g link to `.bashrc`)
```
ln -sv “~/dotfiles/.bash_profile” ~/.bashrc
```
5. Finally, we only need to run:
```
source ~/.bash_profile
```
