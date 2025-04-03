# How to install latest go version on WSL Ubuntu

### Check your shell. I am using `zsh`.
```sh
which $SHELL
```

### Remove old go setup.
```sh
sudo rm -rf /usr/local/go
```

### Download go from source using `wget`. [Current version is 1.24.2.](https://go.dev/dl/go1.24.2.linux-amd64.tar.gz). Check latest version [from](https://go.dev/dl/).
```sh
wget https://go.dev/dl/go1.24.2.linux-amd64.tar.gz
```

### Decompress and extract compressed tar archive to /usr/local.
```sh
sudo tar -C /usr/local -xzf go1.24.2.linux-amd64.tar.gz
```

### Add Go binary to PATH environment variable. I am adding to `.zshrc`.
```sh
vim .zshrc
```
#### Press `i` for insert mode. Add command at below to the end of the file. Press `esc` then `:wq` then `enter`
```sh
export PATH=$PATH:/usr/local/go/bin
```

### Open new shell and check go version
```sh
go version
```