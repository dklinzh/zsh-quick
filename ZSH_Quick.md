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
* To set zsh as your default shell.
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

* Enabling Plugins
Once you spot a plugin (or several) that you'd like to use with Oh My Zsh, you'll need to enable them in the `.zshrc` file. You'll find the zshrc file in your `$HOME` directory. Open it with your favorite text editor and you'll see a spot to list all the plugins you want to load. For example, this might begin to look like this:
```shell
plugins=(
  git
  zsh-completions
  ...
)
```

* Restart zsh (such as by opening a new instance of your terminal emulator) or reload zsh:
```shell
source ~/.zshrc
```

* Using Plugins
Most plugins include a __README__, which documents how to use them.

### Custom Plugins
* If you want to override any of the default behaviors, just add a new file (ending in `.zsh`) in the `custom/` directory.
* If you have many functions that go well together, you can put them as a `XYZ.plugin.zsh` file in the `custom/plugins/` directory and then enable this plugin.
* If you would like to override the functionality of a plugin distributed with Oh My Zsh, create a plugin of the same name in the `custom/plugins/` directory and it will be loaded instead of the one in `plugins/`.

*Clone these repositories in oh-my-zsh's custom plugins directory:*

#### [zsh-completions](https://github.com/zsh-users/zsh-completions)
```shell
git clone https://github.com/zsh-users/zsh-completions ~/.oh-my-zsh/custom/plugins/zsh-completions
```

#### [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

#### [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
[Why must zsh-syntax-highlighting.zsh be sourced at the end of the .zshrc file?](https://github.com/zsh-users/zsh-syntax-highlighting#why-must-zsh-syntax-highlightingzsh-be-sourced-at-the-end-of-the-zshrc-file)

#### [zsh-history-substring-search](https://github.com/zsh-users/zsh-history-substring-search)
```shell
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```
If you want to use `zsh-syntax-highlighting` along with this script, then make sure that you load `zsh-syntax-highlighting` **before** you load `zsh-history-substring-search`:
```shell
plugins=(
  ...
  zsh-syntax-highlighting
  zsh-history-substring-search
)
```

#### [zaw](https://github.com/zsh-users/zaw)
```shell
git clone git://github.com/zsh-users/zaw.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zaw
```

#### [autojump](https://github.com/wting/autojump)
#### [z](https://github.com/rupa/z)
#### [z.lua](https://github.com/skywind3000/z.lua)

### Themes

We'll admit it. Early in the Oh My Zsh world, we may have gotten a bit too theme happy. We have over one hundred themes now bundled. Most of them have [screenshots](https://github.com/robbyrussell/oh-my-zsh/wiki/Themes) on the wiki. Check them out!

#### Selecting a Theme

_Robby's theme is the default one. It's not the fanciest one. It's not the simplest one. It's just the right one (for him)._

Once you find a theme that you'd like to use, you will need to edit the `~/.zshrc` file. You'll see an environment variable (all caps) in there that looks like:

```shell
ZSH_THEME="robbyrussell"
```

To use a different theme, simply change the value to match the name of your desired theme. For example:

```shell
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# see https://github.com/robbyrussell/oh-my-zsh/wiki/Themes#agnoster
```

_Note: many themes require installing the [Powerline Fonts](https://github.com/powerline/fonts) in order to render properly._

In case you did not find a suitable theme for your needs, please have a look at the wiki for [more of them](https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes).