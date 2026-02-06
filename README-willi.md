
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

4. flash:
- left: mod-1, right: mod-3
- find device `diskutil list` (grep "ADV360PRO")
- `diskutil mount /dev/diskN`, mounts to /Volumes/ADV360PRO/
- cp firmware/...-clique.uf2 /Volumes/ADV360PRO/
