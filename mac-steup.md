# Setup notes

## Homebrew

1. Install homebrew: [instructions](https://brew.sh/)
2. Use the `Brewfile` to install all brew things: `brew bundle --file <path-to-brewfile`

## Setup python

### pyenv

```bash
brew install pyenv
pyenv install 3.9.1
pyenv global 3.9.1
pyenv rehash

# confirm
which python
python --version
```

- `pyenv` takes care of pip

## Setup alfred

- Run alfred and allow it to set itself up
- Map alfred to `cmd+Space`, spotlight to `option+Space`

## Setup iterm

- Get the gruvbox theme: [link](https://raw.githubusercontent.com/herrbischoff/iterm2-gruvbox/master/gruvbox.itermcolors)
- Set the font to fira-code
- Turn off the bell

## git

[setup instructions](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Sane defaults

```sh
defaults write com.apple.mail DisableInlineAttachementViewing --bool YES
```

## Fingerprint for `sudo` auth

Edit the file `/private/etc/pam.d/sudo` and paste the following as line 2:

```
auth	sufficient	pam_tid.so
```

Commenting/uncommenting this line will allow authentication of the `sudo` command to be performed using Touch ID.

