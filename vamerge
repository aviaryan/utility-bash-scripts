#!/bin/bash
fn=${1%.*}_hdvid
ffmpeg -i "$2" -acodec libmp3lame "tttmp.mp3"
ffmpeg -i "$1" -i "tttmp.mp3" -c:v libx264 -c:a copy "$fn.mp4"
rm tttmp.mp3
rm "$1"
rm "$2"
# webm to mp4 issue - http://superuser.com/questions/873485/how-to-combine-webm-and-opus-to-generate-mp4
#ffmpeg -i "$1" -i "$2" -acodec copy -vcodec copy "$3"
# https://kwizzu.com/construct.html
