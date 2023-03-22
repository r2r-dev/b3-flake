nix flake for [b3](https://github.com/dannykopping/b3) strace to json parser

Example usage:
```
nix build git+https://github.com/r2r-dev/b3-flake#default

# list opened files of a process
strace -e trace=open,openat -f cat /etc/motd |& ./result/bin/b3 | jq .args[1]
```

![example](https://user-images.githubusercontent.com/39031033/227059163-f9249cb5-706c-46e7-a2a5-c1e15fcd7465.gif)
