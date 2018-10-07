# Useful BASH scripts

Utility bash scripts to do stuff like download youtube videos, download music from youtube, kill dangling Docker images, etc.


## PRO-TIP

For best results, clone this git repo to a fixed location on your computer and add it to `$PATH`.

```sh
cd ~
git clone git@github.com:aviaryan/utility-bash-scripts.git scripts
cd scripts
export PATH="$(pwd):$PATH"
```


## SCRIPTS

### Download video from YouTube in MP4 format

This script requires [youtube-dl](https://github.com/rg3/youtube-dl).

```sh
youtube-video "https://www.youtube.com/watch?v=HgfojLtSBTM"
```

### Merge video and audio together

Requires [ffmpeg](https://www.ffmpeg.org/).

```sh
vamerge <path to video file> <path to audio file>
# the order is important, first video, then audio
```

### Download audio from YouTube in OGG format

This script requires [youtube-dl](https://github.com/rg3/youtube-dl).

```sh
youtube-music "https://www.youtube.com/watch?v=HgfojLtSBTM"  
```

### Convert audio file to OGG

Requires [ffmpeg](https://www.ffmpeg.org/).

```sh
toogg <path to file>
```

### Convert audio file to MP3

Requires [ffmpeg](https://www.ffmpeg.org/).

```sh
tomp3 <path to file>
```

### Uglify a JS code

Dependencies: [Uglijy-JS](https://www.npmjs.com/package/uglify-js).

```sh
uglify <input JS file> <output file>
```

### Download audio from SoundCloud

Dependencies: [Soundscrape](#soundscrape)

```sh
soundcloud-music <link to soundcloud>
```


## DEPENDENCIES

#### ffmpeg

Download from https://www.ffmpeg.org/ and add it to `PATH`.

#### youtube-dl

```
pip install youtube-dl
```

#### soundscrape

```
pip install soundscrape
```

#### UglifyJS

https://www.npmjs.com/package/uglify-js

```
npm install -g uglify-js
```
