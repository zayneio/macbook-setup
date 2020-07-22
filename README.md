# Configuring your dev environment on a new MacBook:

## Useful Links
- Homebrew: https://brew.sh/
- iTerm: https://www.iterm2.com/
- VSCode: https://code.visualstudio.com/
- Sublime: https://www.sublimetext.com/
- Oh-my-zsh: https://ohmyz.sh/

### Install iterm
https://www.iterm2.com/

### Install a code editor
- VSCode: https://code.visualstudio.com/
- Sublime: https://www.sublimetext.com/

For VScode:
Open the app and type in `command + shift P`
Type in `shell` command and click the result to add the shell shortcut so that you can use the `code` shortcut from your terminal to open directories.


### Install homebrew:
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"```

Disable homebrew analytics from tracking you if you’d like:  
```brew analytics off```

### Install git  
```brew install git```


### Github

For getting all set up with github, You may need to do the following:
Generate a new key  
```ssh-keygen -t rsa -b 4096 -C "your_email@example.com"```

Copy the new rsa key:  
```pbcopy < ~/.ssh/id_rsa.pub```

Add this key to your GitHub account.

configure your github user:  
```git config --global user.name ‘username’```  
```git config --global user.email ‘your_email@example.com’```

### Instal Zsh
https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH  
```brew install zsh```

### Install oh-my-zsh
```sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```


### Set zsh as your default shell
If you don’t get prompted to do this when installing oh-my-zsh, try this:   
```chsh -s /usr/local/bin/zsh```

Downloading and changing zsh themes:  
```git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k```
```ZSH_THEME="powerlevel9k/powerlevel9k"```


Additional reading for zsh config:  
https://www.freecodecamp.org/news/how-to-configure-your-macos-terminal-with-zsh-like-a-pro-c0ab3f3c1156/
Importing themes, item colors, fonts, etc.

Item 2 color schemes:   
https://github.com/mbadolato/iTerm2-Color-Schemes

### Installing Ruby
ruby is probably already installed on your Macbook. You can check to confirm with:  
```ruby -v```

You can also install ruby with homebrew:  
```brew install ruby```

### Install a ruby version manager
You'll probably want to use a version mgmt tool like rbenv, rvm, or asdf.

### Using rbenv
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

### Using asdf
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
