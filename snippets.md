# Snippets

## `bash`

### Fast pngquant for osx

```bash
find . -name '*.png' -print0 | xargs -0 -P`sysctl -n hw.ncpu` -L1 pngquant --ext .png --verbose --force --speed 1 --quality 15-55 32
```

### Recursively remove `*.pyc` files

_Source: <http://stackoverflow.com/a/785534>_

```bash
find . -name "*.pyc" -exec rm -rf {} \;
```


## `git`

### Interactive stage

```bash
git add -p
```

### Inline commit message

```bash
git commit -m 'I am a message'
```

### Set default text editor

_Source: <https://stackoverflow.com/a/2596835>_

```bash
# Get current editor
git config --global core.editor
# Set to sublime (requires `subl` command)
git config --global core.editor 'subl --new-window --wait'
# Set to vs-code (requires `code` command)
git config --global core.editor 'code --wait'
```
