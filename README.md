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
2. Install Vundle: https://github.com/VundleVim/Vundle.vim
3. Create a tmux configuration file at `~/.tmux.conf`
4. Follow the installation instructions in https://robots.thoughtbot.com/seamlessly-navigate-vim-and-tmux-splits
5. Install Teamocil: https://github.com/remiprev/teamocil
6. Create a teamocil template, see below for example
7. If you need to resize any of your tmux panes, you can do so in the
   teamocil template, by running an additional tmux command after init,
such as `- tmux resize-pane -t 0 -x 200`
8. Load your color scheme into iTerm by navigating to
   Preferences>Profiles>[your profile]>colors>load presets>import
9. Set your color scheme by selecting it in the dropdown
10. Within iTerm, run `tmux`
11. Within tmux, run `teamocil <your template>`

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
