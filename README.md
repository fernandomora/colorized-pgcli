## Install pgcli:

<https://github.com/dbcli/pgcli>

```
brew install --build-from-source pgcli
```

## Install grc:

<https://github.com/pengwynn/grc>

```
brew install grc
```

## Clone colorized-pgcli:

```
git clone git://github.com/fernandomora/colorized-pgcli ~/.colorized-pgcli
```

## Link to config files from cloned repo:

```
mkdir -p ~/.config/pgcli
ln -svi ~/.colorized-pgcli/.config/pgcli/config ~/.config/pgcli/config
```

```
mkdir -p ~/.grc
ln -svi ~/.colorized-pgcli/.grc/conf.psql ~/.grc/conf.psql
```

## Alias pgcli command to pgcli using grc filtered pager: 

```
alias pgcli="PAGER='grcat ~/.grc/conf.psql | less -iMSx4FXRe' pgcli"
```

#### To make it persistent in zsh:
```
echo "alias pgcli=\"PAGER='grcat ~/.grc/conf.psql | less -iMSx4FXRe' pgcli\"" >> ~/.zshrc
```

## Extra step: Install heroku addon for pgcli:

<https://github.com/chrisanderton/heroku-pg-pgcli>

```
heroku plugins:install git@github.com:chrisanderton/heroku-pg-pgcli.git
```
