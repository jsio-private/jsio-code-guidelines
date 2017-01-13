# Snippets

## `bash`

### Fast pngquant for osx

```bash
find . -name '*.png' -print0 | xargs -0 -P`sysctl -n hw.ncpu` -L1 pngquant --ext .png --verbose --force --speed 1 --quality 15-55 32
```