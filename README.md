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

Install git  
```brew install git```

optional: Check git version
```git —version```


For getting set up with github, You may need to do the following:
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


