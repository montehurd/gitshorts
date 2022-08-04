# gitshorts

&nbsp;

## Motivation

When using Git on the command line, I found myself continually wanting to see:
- **branches** I had locally and which was checked out
- **logs** of recent commits with short commit messages
- **status** of files in the currently checked out branch
- **diffs** of modified but uncommitted files
- **commits** and their file diffs

&nbsp;

## Approach

These scripts make seeing everything mentioned above extremely easy. After installation, simply change to a directory under Git source control, then type `aaa` and press enter. You will see output formatted similar to the following:

![Example output](https://raw.github.com/montehurd/gitshorts/master/screenshot.png)

The repeating sequence `aaa` was chosen to represent showing "All" the info mentioned [above](#user-content-motivation).

Note in the picture above there are six other three-character codes. Three-character repeating codes are extremely easy to invoke. They represent the individual parts of the output displayed when `aaa` is invoked:

- `bbb`
    - **branches**, also indicating which branch is checked out
- `lll`
    - **log** of most recent commits with optional numeric argument (defaults to 5 if unspecified)
- `sss`
    - **status** of files
- `ddd`
    - **diff** for each modified but as-of-yet uncommitted file. once activated use arrow keys to navigate between individual file diffs. use `q` to exit back to `aaa`
- `ccc`
    - **commits**, showing diff for each historical commit. once activated use arrow keys to navigate between individual commit diffs. most recent commit diff is shown first. use `q` to exit back to `aaa`
- `ppp`
    - **prompt**, clearing other console text

&nbsp;

## Installation

If this looks useful, installation is fairly easy:

- run `git clone https://github.com/montehurd/gitshorts.git`
- add `export PATH=$PATH:$HOME/gitshorts` to the bottom of your terminal config file. i.e. `~/.zshrc`, `~/.bashrc` or `~/.profile` etc. this basically routes the three-character commands to their respective scripts
- restart your terminal program or reload your particular terminal's config file: i.e. `source ~/.bashrc`, `source ~/.zshrc` or `source ~/.profile` etc

&nbsp;

## Tweaks

Each of the three-character codes simply invokes a shell script file named with that three-character code. These scripts can be easily modified as needed - just edit the respective file.

&nbsp;

## Known issues

When using `ccc` or `ddd` and viewing very long diffs, I don't know how to scroll the terminal up to the top in a platform independent way:

https://github.com/montehurd/gitshorts/issues/1