## Install pgcli

<https://github.com/dbcli/pgcli>

```
brew install --build-from-source pgcli
```

## Install grc

<https://github.com/pengwynn/grc>

```
brew install grc
```

## Clone colorized-pgcli

```
git clone git://github.com/fernandomora/colorized-pgcli ~/.colorized-pgcli
```

## Create link config files from cloned repo

```
mkdir -p ~/.config/pgcli
ln -sf ~/.colorized-pgcli/.config/pgcli/config ~/.config/pgcli/config
```

```
mkdir -p ~/.grc
ln -sf ~/.colorized-pgcli/.grc/conf.psql ~/.grc/conf.psql
```

## Alias psql command to pgcli using grc filtered pager 

```
alias psql="PAGER='grcat ~/.grc/conf.psql | less -iMSx4FXRe' pgcli"
```

#### To make it persistent in zsh
```
echo "alias psql=\"PAGER='grcat ~/.grc/conf.psql | less -iMSx4FXRe' pgcli\"" >> ~/.zshrc
```

## Extra step: Install heroku addon for pgcli

<https://github.com/chrisanderton/heroku-pg-pgcli>

```
heroku plugins:install git@github.com:chrisanderton/heroku-pg-pgcli.git
```
