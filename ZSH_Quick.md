# [ZSH](https://www.zsh.org/)
```shell
git clone https://git.code.sf.net/p/zsh/code zsh-code
```

## [Installation](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
### macOS
* Try `zsh --version` before installing it from Homebrew. If it's newer than **4.3.9** you might be OK. Preferably newer than or equal to **5.0**.  

*via [Homebrew](https://brew.sh/)*
```shell
brew install zsh zsh-completions
```

To set zsh as your default shell.
```shell
chsh -s /bin/zsh
```
* **Log out and login back again to use your new default shell.**  
* Test that it worked with `echo $SHELL`. Expected result: `/bin/zsh` or similar.  
* Test with `$SHELL --version`. Expected result: `zsh 5.3 (x86_64-apple-darwin18.0)` or similar.

## [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
Oh My Zsh is installed by running one of the following commands in your terminal. You can install this via the command-line with either `curl` or `wget`.  

*via curl*
```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

*via wget*
```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### [Plugins](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins)
Oh My Zsh comes with a shitload of plugins to take advantage of. You can take a look in the [plugins](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins) directory and/or the [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) to see what's currently available.

#### Enabling Plugins
Once you spot a plugin (or several) that you'd like to use with Oh My Zsh, you'll need to enable them in the `.zshrc` file. You'll find the zshrc file in your `$HOME` directory. Open it with your favorite text editor and you'll see a spot to list all the plugins you want to load. For example, this might begin to look like this:
```shell
plugins=(
  git
  osx
  ...
)
```

#### Using Plugins
Most plugins include a __README__, which documents how to use them.

### Custom Plugins
If you want to override any of the default behaviors, just add a new file (ending in `.zsh`) in the `custom/` directory.

If you have many functions that go well together, you can put them as a `XYZ.plugin.zsh` file in the `custom/plugins/` directory and then enable this plugin.

If you would like to override the functionality of a plugin distributed with Oh My Zsh, create a plugin of the same name in the `custom/plugins/` directory and it will be loaded instead of the one in `plugins/`.

#### [zsh-completions](https://github.com/zsh-users/zsh-completions)
