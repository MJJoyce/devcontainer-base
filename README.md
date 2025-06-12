# devcontainer-base
Base dev container configuration repository

# Usage

This requires DevPod and Docker to be installed and configured.

```
# Install DevPod
curl -L -o devpod "https://github.com/loft-sh/devpod/releases/latest/download/devpod-darwin-arm64" && sudo install -c -m 0755 devpod /usr/local/bin && rm -f devpod

# Add Docker as a Provider
devpod provider add docker
```

1. Clone [devcontainer-base](https://github.com/MJJoyce/devcontainer-base) repository. Name this repo clone with the name you want for your new container environment. `cd` into the new folder.
2. Update the output container name with a unique name.
3. Create a new dev container with `DevPod`

```
devpod up . --dotfiles git@github.com:MJJoyce/dots.git --ide none --dotfiles-script=install_devpod.sh
```

4. SSH to the new dev container to finish setup: `devpod ssh` and then select the relevant environment.
5. Open `vim` to auto install plugins and dependencies.

Your dev container is ready for use.
