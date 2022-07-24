gitshorts
=========

Bash scripts for super quick Git info.

<i>tldr: Reduced ~90% of the Git commands I used to type on a regular basis to typing “aaa &lt;enter&gt;”.</i>

Run "git clone https://github.com/montehurd/gitshorts.git" from your user directory to place the shortcut files in a "~/gitshorts" folder.

Then add "export PATH=$PATH:$HOME/gitshorts" to your "~/.zshrc" or "~/.bashrc" file.

Then in terminal, change to a directory managed by Git and type "aaa" enter.

This should print to the terminal a set of useful info about the state of the Git repo.

![Example output](https://raw.github.com/montehurd/gitshorts/master/screenshot.png)

Each section of the output of "aaa" has a header. Each header references the shortcut to enter if you want just that section's info - for example, the "Log" section can be quickly invoked by typing "lll 50" to print a pretty log of the last 50 changes to the repo.

Notice each of the shortcuts are a single character repeated 3 times. This is why it's such a time saver.