# Useful BASH scripts

Utility bash scripts to do stuff like download youtube videos, download music from youtube, kill dangling Docker images, etc.


## PRO TIP

For best results, clone this git repo to a fixed location on your computer and add it to `$PATH`.

```sh
cd ~
git clone git@github.com:aviaryan/utility-bash-scripts.git scripts
cd scripts
export PATH="$(pwd):$PATH"
```

## SCRIPTS

### Download video from YouTube in MP4

This script requires [youtube-dl](https://github.com/rg3/youtube-dl).

```sh
youtube-video https://www.youtube.com/watch?v=HgfojLtSBTM
```

### Merge video and audio together

Requires [ffmpeg](https://www.ffmpeg.org/).

```sh
vamerge <path to video file> <path to audio file>
# the order is important, first video, then audio
```
