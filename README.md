# New Macbook Setup

## Useful Links
- Homebrew: https://brew.sh/
- iTerm: https://www.iterm2.com/
- VSCode: https://code.visualstudio.com/
- Sublime: https://www.sublimetext.com/
- Oh-my-zsh: https://ohmyz.sh/

## Install iTerm2
https://www.iterm2.com/  

```shell
brew cask install iterm2
```  

*(Note: See below for installing homebrew)*

## Install a Code Editor
### VSCode
https://code.visualstudio.com/

```shell
brew cask install visual-studio-code
```  

**Shortcut For VSCode:**
Open the VSCode app and type in `command + shift P`, then type in `shell command` and click the search result. This will add a shortcut so that you can use `code` to open files and directories from your terminal in VSCode. For example, to open the directory you're currently in:

```shell
code .
```  

### Sublime 
https://www.sublimetext.com/

```shell
brew cask install sublime-text
```  

**Shortcut for Sublime**
```shell
ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl
```  

## Install homebrew
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"```

Disable homebrew analytics if you want:  
```brew analytics off```

## Install git  
```brew install git```


## Github
For getting set up with github, You may need to do the following:
- Generate a new key:  
```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```

- Copy the new rsa key:  
```pbcopy < ~/.ssh/id_rsa.pub```

- Add this key to your GitHub account

Additionally, you can configure your github user:  
```git config --global user.name ‘username’```  
```git config --global user.email ‘your_email@example.com’```

## Instal Zsh
https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH  
```brew install zsh```

## Install oh-my-zsh
```sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```


## Set zsh as your default shell
If you don’t get prompted to do this when installing oh-my-zsh, try this:   
```chsh -s /usr/local/bin/zsh```

Additional reading for zsh config, covers themes, colors, fonts, etc:  
https://www.freecodecamp.org/news/how-to-configure-your-macos-terminal-with-zsh-like-a-pro-c0ab3f3c1156/

Iterm2 color schemes:   
https://github.com/mbadolato/iTerm2-Color-Schemes

## Installing Ruby
ruby is probably already installed on your Macbook. You can check to confirm with:  
```ruby -v```

You can also install ruby with homebrew:  
```brew install ruby```

## Install a ruby version manager
You'll probably want to use a version mgmt tool like rbenv, rvm, or asdf.

## rbenv
```brew install rbenv```  
```rbenv init```  
Follow the printed instructions to set up rbenv shell integration.  
Upgrade with:  
```brew upgrade rbenv ruby-build```

Basic Useage:  
```shell
# list all available versions:
rbenv install -l

# install a Ruby version:
rbenv install 2.0.0-p247

# Set the ruby version locally
rbenv local 1.9.3-p327

# Set the ruby version globally
rbenv global 1.8.7-p352
```

## asdf
```brew install coreutils curl git```  
```brew install asdf```  

Add this to ~/.zshrc  
```. $(brew --prefix asdf)/asdf.sh```  

Upgrade with:  
```brew upgrade asdf```  

Basic Usage:  
```shell
# Add something
asdf plugin add ruby

# List plugins
asdf plugin list

# Update plugins
asdf plugin update --all

# Remove something
asdf plugin remove

# Install a specific version
asdf install ruby 2.6.5

# Set global version
asdf global ruby 2.6.5

# Set local version
asdf local ruby 2.6.5
```  

## XCode
You will probably need to install xcode at some point. Try this:
```shell
xcode-select --install
```  

## Postgres
To install:
```shell
brew install postgres
``` 

To start:
```shell
brew services start postgresql
```  


## Rails

```shell
sudo gem install rails
```

## Bundler

```shell
gem install bundler
```

## Node
```shell
brew install node
```  

## Deno
```shell
brew install deno
```  

## Elixir
```shell
brew install elixir
```  
