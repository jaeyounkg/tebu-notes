# When you are not root
## Installing `fish`
Just install it locally, in the home directory
```bash
git clone --depth=1 https://github.com/fish-shell/fish-shell
cd fish-shell
mkdir build
cd build

cmake -DCMAKE_INSTALL_PREFIX=$HOME/.local ..
make
make install
```

## Replacing `bash` with `fish`
Put this in `~/.bashrc`:
```bash
if [ -x "$HOME/local/bin/fish" ]; then
    exec "$HOME/local/bin/fish"
fi
```