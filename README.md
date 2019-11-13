# 🤓 Utility bash scripts

[![Contributors needed](https://img.shields.io/badge/contributors-needed-yellow.svg)](.github/CONTRIBUTING.md) [![Build Status](https://travis-ci.org/aviaryan/utility-bash-scripts.svg?branch=master)](https://travis-ci.org/aviaryan/utility-bash-scripts)

Utility bash scripts to do automatable tasks with a single command. We have scripts to download youtube videos, download music from youtube, convert media files, etc. 

<u>Contribute and add your secret script.</u>

## 📝 NOTES

Download scripts download to `~/Downloads/` folder. For videos, they download to `~/Downloads/Videos` and for audio, they download to `~/Downloads/Music`.

For best results, clone this git repo to a fixed location on your computer and add it to `$PATH`.
```sh
cd ~
git clone https://github.com/aviaryan/utility-bash-scripts.git utility-scripts
cd utility-scripts
export PATH="$(pwd):$PATH"
```


## 📜 SCRIPTS

### 🔻 Download video from YouTube in MP4 format

Script: [youtube-video](youtube-video)  
Dependencies: [youtube-dl](https://github.com/rg3/youtube-dl), [ffmpeg](https://www.ffmpeg.org/), [aria2c](https://aria2.github.io/) (optional)

```sh
youtube-video "https://www.youtube.com/watch?v=HgfojLtSBTM"
```

### 🔀 Merge video and audio together

Script: [vamerge](vamerge)  
Dependencies: [ffmpeg](https://www.ffmpeg.org/)

```sh
vamerge <path to video file> <path to audio file>
# the order is important, first video, then audio
```

### 🔰 Download audio from YouTube

Script: [youtube-music](youtube-music)  
Dependencies: [youtube-dl](https://github.com/rg3/youtube-dl), [ffmpeg](https://www.ffmpeg.org/), [aria2c](https://aria2.github.io/) (optional)

*Default download format is `ogg`(vorbis), pass second parameter as `mp3`, `wav`, `m4a` to use another format.*

```sh
youtube-music "https://www.youtube.com/watch?v=HgfojLtSBTM"  
youtube-music "https://www.youtube.com/watch?v=HgfojLtSBTM" mp3
```

### ♋️ Convert audio file to OGG

Script: [toogg](toogg)  
Dependencies: [ffmpeg](https://www.ffmpeg.org/)

```sh
toogg <path to file>
```

### 😈 Uglify a JS code

Script: [uglify](uglify)  
Dependencies: [Uglify-JS](https://www.npmjs.com/package/uglify-js)

```sh
uglify <input JS file> <output file>
```

### ✂️ Extract any archive

Script: [extract](extract)  
Dependencies: [tar](https://www.gnu.org/software/tar/), [gzip](https://www.gnu.org/software/gzip/), [p7zip](https://www.7-zip.org/), [bzip2](http://www.bzip.org/)

*Extracting .dmg files works only on MacOS.*

```sh
extract <path to archive>
```

### ♋️ Convert audio file to MP3

Script: [tomp3](tomp3)  
Dependencies: [ffmpeg](https://www.ffmpeg.org/)

```sh
tomp3 <path to file>
```

### 🔉 Download audio from SoundCloud

Script: [soundcloud-music](soundcloud-music)  
Dependencies: [Soundscrape](https://github.com/Miserlou/SoundScrape)

```sh
soundcloud-music <link to soundcloud>
```

### 🐳 Force stop and clean Docker containers

Script: [dckill](dckill)

```sh
dckill
```

### ♻️ Empty Trash folder

Script: [empty-trash](empty-trash)

```sh
empty-trash
```

### ⏰ Get current time at any timezone

Script: [clock](clock)  
Dependencies: [timedatectl for Linux](https://www.freedesktop.org/software/systemd/man/timedatectl.html), sudo access for Mac

```sh
clock list
clock <Time Zone>
```

### 🌧 Get weather report for a location

Script: [weather](weather)

```sh
weather <City Name>
weather # Will use your IP Address location
```

### 🏹 Create custom short link for a GitHub URL using git.io

Script: [gh-url](gh-url)

```sh
gh-url <url-to-shorten> <short-code>
```

### 🤐 ZIP without .DS_Store on a Mac

Script: [maczip](maczip)

```sh
maczip <path to folder>
```

### 🖼 Delete screenshots from Desktop on a Mac

Script: [delete-ss](delete-ss)

```sh
delete-ss
```

### ❌ Remove .DS_Store files recursively (Mac)

Script: [rm-ds-store](rm-ds-store)

```sh
rm-ds-store
```

### 🖼 Show certificate information of a service

Script: [show-certificate](show-certificate)  
Dependencies: [openssl](https://www.openssl.org/)

```sh
show-certificate google.com
```

### 📹 Encode video to x265

Script: [encode-x265](encode-x265)  
Dependencies: [ffmpeg](https://pkgs.org/download/ffmpeg)

*Default encoded video's name is `videoname-x265`. But you can change it like the second example.*

```sh
encode-x265 <path to video>
encode-x265 <path to video> <path to encoded video>
```

### 🎥 Convert video to gif

Script: [gif-convert](gif-convert)  
Dependencies: [ffmpeg](https://pkgs.org/download/ffmpeg)

```sh
gif-convert <path to video> <path to gif> <start_at> <end_at> <fps> <scale>
```

*If you don't want to change the value, you can use `-`.*

```sh
gif-convert input.mp4 output.gif 05:00 05:03.6 - 640x360 
```

### 📜 Learn a new command

Script: [learn](learn)  
Dependencies: [cowsay](https://github.com/schacon/cowsay)

```sh
learn
```

### 🍅 Pomodoro

Script: [pomodoro](pomodoro)

```sh
pomodoro <focus time length> <break time length>
```

## 🤘🏻 SIMPLE BASH COMMANDS

These commands are so easy to use that creating a script for them would be overkill.

### 🗄 Display filesystem information (disk usage, mount path)

```sh
df
```
