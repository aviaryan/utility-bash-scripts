# Utility bash scripts

Utility bash scripts to do automatable tasks with a single command. We have scripts to download youtube videos, download music from youtube, convert media files, etc. 

👥 Contribute and add your secret script.

## NOTES

Download scripts download to `~/Downloads/` folder. For videos, they download to `~/Downloads/Videos` and for audio, they download to `~/Downloads/Music`.

For best results, clone this git repo to a fixed location on your computer and add it to `$PATH`.
```sh
cd ~
git clone https://github.com/aviaryan/utility-bash-scripts.git utility-scripts
cd utility-scripts
export PATH="$(pwd):$PATH"
```


## SCRIPTS

### Download video from YouTube in MP4 format

*Dependencies*: [youtube-dl](https://github.com/rg3/youtube-dl), [ffmpeg](https://www.ffmpeg.org/)

```sh
youtube-video "https://www.youtube.com/watch?v=HgfojLtSBTM"
```

### Merge video and audio together

*Dependencies*: [ffmpeg](https://www.ffmpeg.org/)

```sh
vamerge <path to video file> <path to audio file>
# the order is important, first video, then audio
```

### Download audio from YouTube in OGG format

*Dependencies*: [youtube-dl](https://github.com/rg3/youtube-dl), [ffmpeg](https://www.ffmpeg.org/)

```sh
youtube-music "https://www.youtube.com/watch?v=HgfojLtSBTM"  
```

### Convert audio file to OGG

*Dependencies*: [ffmpeg](https://www.ffmpeg.org/)

```sh
toogg <path to file>
```

### Convert audio file to MP3

*Dependencies*: [ffmpeg](https://www.ffmpeg.org/)

```sh
tomp3 <path to file>
```

### [Uglify a JS code](uglify)

*Dependencies*: [Uglify-JS](https://www.npmjs.com/package/uglify-js)

```sh
uglify <input JS file> <output file>
```

### Download audio from SoundCloud

*Script*: [soundcloud-music](soundcloud-music)
*Dependencies*: [Soundscrape](https://github.com/Miserlou/SoundScrape)

```sh
soundcloud-music <link to soundcloud>
```

### Force stop and clean Docker containers

*Script*: [dckill](dckill)

```sh
dckill
```
