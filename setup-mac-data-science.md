### So, you got a Brand New MAC 🍺


- Install XCode
- Install Packages

  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  # Install oh-my-zsh
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
  brew install git
  brew install tldr
  brew install pyenv
  brew install httpie
  brew install go
  brew install --cask amethyst
  brew install --cask iterm2
  brew install wget
  ```
- Python 🐍 Installation
  
  ```
  PATH=$(pyenv root)/shims:$PATH # in your (z|ba)shrc file before exporting PATH
  pyenv install -v 3.9.0
  pyenv global 3.9.0
  # Install Poetry
  curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
  ```
- Install Docker (increase memory or atleast make a note of this in your mind if some data science images don't work)
- Download Spotify and configure ZSH plugin for spotify

- CLI Starters

```
bat: a better cat 
tldr: man which actually helps
fd: works like find 
starship: terminal with benefits
z: To learn the directories used
Httpie: http requests was never easier
ncdu: Disk usage analyzer
```

- Apps
  - Amethyst - Window manager

    **shortcuts**
    ```
    Alt + shift + . (Decrease window Pane count)
    Alt + shift + , (Increase window pane count)
    Alt + shift + enter (make the current window the main window)
    Alt + shift + space (cycle)
    ```
  - 1Password
    **shortcuts**
    ```
    Alt + command + \  # (Show 1Password Mini)
    ```
- TablePlus
  Visualize those tables
  
- Alfred
  Same as CMD + SHIFT + SPACE but WITH ALT + SHIFT + SPACE 
  
  Favorite Feature. - It can seamlessly search the bookmarks!
