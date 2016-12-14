# Dotfiles Managed with Git Notes

- By using branches and a master for the default you can keep different versions and versioning in general for all configs simultaneously for all systems

- Below is a great snippet from a [HackerNews thread](https://news.ycombinator.com/item?id=11070797) on just this topic

```
git init --bare $HOME/.dotfiles
alias config='/usr/bin/git --git-dir=$HOME/.dotfiles --work-trees=$HOME'
config config status.showUntrackedFiles no
```

- `~/.dotfiles` becomes a bare git repository, where later I'll keep seperate submodules, particularly for bash, vim, i3, Xresources

- Any file within the home folder can be versioned with normal commands like:
```
config status
config add .vimrc
config commit -m "Add vimrc"
config add .config/redshift.conf
config commit -m "Add redshift config"
config push 
```

- You could then clone the configs repository to any new machine with:
 - `git clone --separate-git-dir=$HOME/.


