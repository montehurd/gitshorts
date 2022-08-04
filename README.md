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

The repeating sequence `aaa` was chosen to represent showing "All" the info mentioned above.

Note in the picture above there are six other three-character codes. Three-character repeating codes are extremely easy to invoke. They represent the individual parts of the output displayed when `aaa` is invoked:

- `bbb`
    - **b**ranches, indicating which branch is checked out
- `lll`
    - **l**ist most recent commits with optional number argument which defaults to 5 if unspecified
- `sss`
    - **s**tatus of files in the current Git repo
- `ddd`
    - **d**iff for each modified but as-of-yet uncommitted file. once activated use arrow keys to navigate between individual file diffs, use `q` to exit
- `ccc`
    - **c**ommits, showing diff for each historical commit. use arrow keys to navigate between individual commit diffs, use `q` to exit
- `ppp`
    - clear console output showing empty prompt

&nbsp;

## Installation

If this looks useful, installation is fairly easy.

- run `git clone https://github.com/montehurd/gitshorts.git`
- add `export PATH=$PATH:$HOME/gitshorts` to the bottom of your `~/.zshrc` or `~/.bashrc` file
- reload your .bashrc or .zshrc file settings: `source ~/.bashrc` or `source ~/.zshrc`

&nbsp;

## Tweaks

Each of the three-character codes simply invokes a shell script file named with that three-character code. These scripts can be easily modified as needed - just edit the respective file.
