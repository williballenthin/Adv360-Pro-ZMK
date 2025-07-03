
## on macOS

1. Get podman (via nix shell is ok).

2.
```sh
$ podman machine init
$ podman machine start
$ set -g -x DOCKER_HOST 'unix:///var/folders/.../T/podman/podman-machine-default-api.sock'
$ make
```

3. find results in ./firmware

4. mount adv360 via `diskutil list` and `diskutil mount /dev/diskN`
