# Completions

Additional completion definitions for Bash and Zsh.

## List

Zsh:

- https://github.com/robbyrussell/oh-my-zsh/blob/master/plugins/vault/_vault

## Usage

### Zsh

Clone the repo

```shell
git clone https://github.com/modille/completions ~/git/github.com/modille/completions
```

Then include it on `fpath` by adding the following to `~/.zshrc`:

```shell
MODILLE_COMPLETIONS="$HOME/git/github.com/modille/completions/zsh"
[[ -d $MODILLE_COMPLETIONS ]] && fpath=($MODILLE_COMPLETIONS $fpath)
```

And finally source the new changes and rebuild `zcompdump`:

```shell
source ~/.zshrc
rm -f ~/.zcompdump; compinit
```
