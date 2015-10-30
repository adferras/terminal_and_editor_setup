# terminal_and_editor_setup
Instructions for how to setup and configure iTerm2 and Vim on Mac

Resources:
https://robots.thoughtbot.com/seamlessly-navigate-vim-and-tmux-splits

https://github.com/christoomey/vim-tmux-navigator

http://www.dayid.org/os/notes/tm.html

To change your cursor during insert mode:
https://gist.github.com/andyfowler/1195581

Steps:

1. Make sure tmux and vim are installed
2. Install Vundle
2. Create a tmux configuration file at `~/.tmux.conf`
2. Follow the installation instructions in https://robots.thoughtbot.com/seamlessly-navigate-vim-and-tmux-splits
3. Install Teamocil: https://github.com/remiprev/teamocil
6. Create a teamocil template, see below for examples
7. If you need to resize any of your tmux panes, you can do so in the
   teamocil template, by running an additional tmux command after init,
such as `- tmux resize-pane -t 0 -x 200`
8. Open iTerm and run `tmux`
9. Within tmux, run `teamocil <your template>`
