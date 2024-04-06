# Introduction
These are docker images I use on machines where I don't want to clutter my enviroment. Keep in mind that when creating containers, you should usually map a volume so you don't lose work.

# What's next
NixOS. I do not understand how it works yet.

# Usage
## Images
### dotnet8
This images is intended for remote development meaning that you shouldn't need to install anything except VS Code (or [Neo]Vim if you know what you're doing). Using plugins you can connect to the filesystem of the container and create your projects within.

### spotdl
Run a container while you're in the `<path>` using the command `docker run --rm -v <path>:/spotdl <imageid>` where:
- <path> is the absolute path to where your songs.txt is saved (songs/ in image below - image already includes output of the container)
- <imageid> is the id of the docker image

![Working directory](https://github.com/Adrigorithm/docker-images/assets/12832161/eb68e41a-90de-47c7-be0a-224a0dda2dff)

`songs.txt` is a file that is just a list of song urls separated by a space (for example: https://open.spotify.com/track/6I9VzXrHxO9rA9A5euc8Ak?si=9de012e511e74932 https://open.spotify.com/track/0SiywuOBRcynK0uKGWdCnn?si=b8fb064825a14682 https://open.spotify.com/track/5xv4ggemGPNpowZAMwEYHH?si=040a2f48a469458e).

The exact command that was used in the image is `docker run --rm -v C:\Users\DKnig\Documents\Dockerfiles\spotdl\songs:/spotdl 0196292b7e8e808e089037730b899bf79b5da5a187491c90e57be0ef08f67eb1` while working dir was `C:\Users\DKnig\Documents\Dockerfiles\spotdl\songs`

All credits go to the official developers of [spotDL](https://github.com/spotDL/spotify-downloader)

## These images suck
I know, but they work.

# Why
1. "It works on my machine"
2. My supercomputer needs to remain clean to run the best games :)
3. To fuck with you
