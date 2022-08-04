# gitshorts

&nbsp;

## Motivation

When using Git on the command line, I found myself continually wanting to see:
- which branches I had locally and which was checked out
- recent commits and their short commit messages
- status of files in the currently checked out branch
- diff of each modified but uncommitted file
- diff of files comprising historical commits

&nbsp;

## Approach

This repo, once installed, makes seeing everything mentioned above extremely easy. After installation, simply change to a directory under Git source control, then type "aaa" and press enter. You will see output formatted similar to the following:

![Example output](https://raw.github.com/montehurd/gitshorts/master/screenshot.png)

The repeating sequence "aaa" was chosen to represent showing "All" info mentioned above.

Note in the picture above there are six other three-character codes. Three-character repeating codes are extremely easy to invoke. They represent the individual parts of the output displayed when "aaa" is invoked:

- "bbb"
    - lists branches indicating which branch is checked out
- "lll"
    - lists the 5 most recent commits. can be invoked with a number argument to show more/less - ie "lll 50" will show 50 most recent commit messages
- "sss"
    - show status of files in the current Git repo
- "ddd"
    - show diff for each modified but as-of-yet uncommitted file in the current Git repo - use arrow keys to navigate between individual file diffs, use "q" to return to "aaa"
- "ccc"
    - show diff for each historical commit in the current Git repo - use arrow keys to navigate between individual commit diffs, use "q" to return to "aaa"
- "ppp"
    - clear console output showing empty prompt

&nbsp;

## Installation

If this looks useful, installation is fairly easy.

- run `git clone https://github.com/montehurd/gitshorts.git`
- add `export PATH=$PATH:$HOME/gitshorts` to the bottom of your "~/.zshrc" or "~/.bashrc" file
- reload your .bashrc or .zshrc file settings: `source ~/.bashrc` or `source ~/.zshrc`

&nbsp;

## Tweaks

Each of the three-character codes simply invokes a shell script file named with that three-character code. These scripts can be easily modified as needed - just edit the respective file.


&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

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