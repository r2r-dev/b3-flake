nix flake for [b3](https://github.com/dannykopping/b3) strace to json parser

Example usage:
```
nix build git+https://github.com/r2r-dev/b3-flake#default

strace -f cat /etc/passwd |& ./result/bin/b3 | jq -s
```
