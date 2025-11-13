# Fresh installation guide

## Ghostty install

```bash
brew install --cask ghostty
```

## Meslo Nerd Font install
 ```bash
 brew install font-meslo-lg-nerd-font
 ```

## Setup Ghostty config file

1. Create or open the Ghostty configuration file:

```bash
vim ~/.config/ghostty/config
```

Add the configuration in `./ghostty/config`

## Oh my posh install

```bash
brew install jandedobbeleer/oh-my-posh/oh-my-posh
```

2. Add the following snippet as the last line to `~/.zshrc`:

```bash
if [ "$TERM_PROGRAM" != "Apple_Terminal" ]; then
  eval "$(oh-my-posh init zsh)"
fi
```

3. Once added, reload your profile for the changes to take effect.

```bash
exec zsh
```
 4. Copy the theme JSON file located in `./posh/base.json` into a new directory like

```bash
mkdir ~/.poshthemes
cd ~/.poshthemes
vim base.json
```

5. Adjust the Oh My Posh init line in `~/.zshrc` by adding the `--config` flag with the location of your theme file like

```bash
eval "$(oh-my-posh init zsh --config $HOME/.poshthemes/base.json)"
```

6. Once altered, reload your profile for the changes to take effect.

```bash
exec zsh
```

## Setup zsh-autosuggestions plugin

```bash
brew install zsh-autosuggestions
echo "source $(brew --prefix)/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
source ~/.zshrc
```

## Setup zsh-syntax-highlighting

```bash
brew install zsh-syntax-highlighting
echo "source $(brew --prefix)/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
source ~/.zshrc
```

## tmux and zoxide install

1. Install tmux & zoxide with homebrew

```bash
brew install tmux
brew install zoxide
```

2. Then, add the following line to your `~/.zshrc` file to initialize zoxide:

```bash
eval "$(zoxide init zsh)"
```

3. Restart your terminal

```bash
source ~/.zshrc
```