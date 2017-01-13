# Python Version Manager: `pyenv`

This is the nicest version manager for python on OSX that I have found.  It takes some work to set up, but is worth the effort later.

## Getting Started

- We will be using `brew` a lot, make sure you have it.
- Remove old python with: `brew uninstall python`.
  - _Note: You may need to add the `--force` option._
- Follow [pyenv installation instructions](https://github.com/yyuu/pyenv#homebrew-on-mac-os-x).
  - TLDR; `brew update && brew install pyenv`
  - pyenv has [some great docs](https://github.com/yyuu/pyenv/wiki/Common-build-problems) for helping with problematic installations.
- You will likely want to add both of the following lines to your `~/.bash_profile` (as instructed by pyenv installation)
  - `export PYENV_ROOT=/usr/local/var/pyenv`
  - `if which pyenv > /dev/null; then eval "$(pyenv init -)"; fi`
- Start a new bash session
- You should now have a `pyenv` command.  Try it out with `pyenv versions`.


## Using a Specific Version

- Install a new version: `pyenv install 2.7.12`
- Using that version for global python: `pyenv global 2.7.12`
