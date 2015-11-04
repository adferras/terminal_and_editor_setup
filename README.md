# Terminal and editor setup
Instructions for how to setup and configure iTerm2 and Vim on Mac

## Resources:
Tmux command cheat sheet:
http://www.dayid.org/os/notes/tm.html

To change your cursor during insert mode:
https://gist.github.com/andyfowler/1195581

iTerm2 color scheme:
http://ethanschoonover.com/solarized

## Steps:

1. Make sure tmux and vim are installed
2. Modify your `~/.vimrc` file per the following instructions for tmux:
   https://coderwall.com/p/if9mda/automatically-set-paste-mode-in-vim-when-pasting-in-insert-mode
3. Install Vundle: https://github.com/VundleVim/Vundle.vim
4. Create a tmux configuration file at `~/.tmux.conf`
5. Follow the installation instructions in https://robots.thoughtbot.com/seamlessly-navigate-vim-and-tmux-splits
6. Install Teamocil: https://github.com/remiprev/teamocil
7. Create a teamocil template, see below for example
8. If you need to resize any of your tmux panes, you can do so in the
   teamocil template, by running an additional tmux command after init,
such as `- tmux resize-pane -t 0 -x 200`
9. Load your color scheme into iTerm by navigating to
   Preferences>Profiles>[your profile]>colors>load presets>import
10. Set your color scheme by selecting it in the dropdown
11. Setup the ability to copy/paste from tmux/vim using:
    http://evertpot.com/osx-tmux-vim-copy-paste-clipboard/
12. Within iTerm, run `tmux`
13. Within tmux, run `teamocil <your template>`

### Teamocil template:
```
 windows:
   - name: sample_rails_app
     root: ~/Github/sample_rails_app
     layout: main-vertical
     panes:
       - commands:
         - tmux resize-pane -t 1 -x 120
         - vim
       - commands:
         - git status
       - commands:
         - ls
       - commands:
         - bundle exec guard
```

## If you've done it all correctly
This is using the Solarized Dark Higher Contrast color scheme for iTerm2

![Example](/images/tmux\ with\ editor.png)
