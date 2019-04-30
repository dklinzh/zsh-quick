# [ZSH](https://www.zsh.org/)
```
git clone https://git.code.sf.net/p/zsh/code zsh-code
```
## [Installation](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
### macOS
Try `zsh --version` before installing it from Homebrew. If it's newer than **4.3.9** you might be OK. Preferably newer than or equal to **5.0**. 
*[Homebrew](https://brew.sh/)*
```
brew install zsh zsh-completions
```
To set zsh as your default shel.
```
chsh -s /bin/zsh
```
**Log out and login back again to use your new default shell.**
Test that it worked with `echo $SHELL`. Expected result: `/bin/zsh` or similar.
Test with `$SHELL --version`. Expected result: `zsh 5.3 (x86_64-apple-darwin18.0)` or similar.

## [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
Oh My Zsh is installed by running one of the following commands in your terminal. You can install this via the command-line with either `curl` or `wget`.
*via curl*
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
*via wget*
```
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```