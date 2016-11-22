# DOCFILES
## REFERENCES: 
* [Mathiasbynens dotfiles](https://github.com/mathiasbynens/dotfiles)
* [Get started with dotfiles](https://medium.com/@webprolific/getting-started-with-dotfiles-43c3602fd789#.lngfeji1z)

## INTRODUCTION:
   * Dotfiles are used to customize system
   * It can help us to automate all the things

### Some using dotfiles
   * **.bash_profile**: This file in home directory is loaded first. Some people like to put most of their startup configuration in one file.
   * **.alias**: Allow to define shortcuts for commands, to add default arguments, and/or to abbreviate longer one-liners.
   * **.fucntion**: Commands that are too complex for an alias can be defined in a function
   * **.gitignore**: Ignore all the files/folders that you don't want to push it to any version control
   * **.editorconfig**: Define and maintain consistent coding styles between different editors and IDEs 

### Get started
   * Need to organize it as a USB drive. Store it in a version control is great e.g GitHub.
   * Include all files in a folder (e.g /Users/ningo/.dotfiles), then run:

   ```
   for DOTFILE in `find /Users/ningo/.dotfiles`
   do
    [ -f “$DOTFILE” ] && source “$DOTFILE”
   done
   ```

## INSTALL
1. Create new folder *dotfiles*: `mkdir dotfiles`
2. `cd dotfiles/`
3. Clone code from: `git@github.com:ningo-asnet/dotfiles.git`
4. Then link files from cloned folder to home: 

  **OSX**
  (E.g link to `.bash_profile`)
  ```
  ln -sv “~/dotfiles/.bash_profile” ~
  ```

  **Ubuntu**
  (E.g link to `.bashrc`)
  ```
  ln -sv “~/dotfiles/.bash_profile” ~/.bashrc
  ```

5. Finally, we only need to run:
```
source ~/.bash_profile
```
