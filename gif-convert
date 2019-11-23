#!/usr/bin/env bash

# Tips 
# ------
# If you want to keep aspect ratio when scaling you just need to specify one component either width/height and the other set to -1.
# Example: gif-convert input.mp4 output.gif - - - -1:360
# If the video's resolution is 1280x720 then -1:360 = 640x360

start_at=0
end_at="$(ffmpeg -i "$1" 2>&1 | grep "Duration" | cut -d ' ' -f 4 | sed s/,//)"
fps="$(ffmpeg -i "$1" 2>&1 | grep "fps" | grep -o "[0-9.]*.fps" | grep -o "[0-9.]*")"
scale="$(ffmpeg -i "$1" 2>&1 | grep "fps" | grep -Po "\d{3,5}x\d{3,5}")"

if [[ $3 != "-" ]]; then start_at="$3"; fi
if [[ $4 != "-" ]]; then end_at="$4"; fi
if [[ $5 != "-" ]]; then fps="$5"; fi
if [[ $6 != "-" ]]; then scale="$6"; fi

# Generate color pattern
ffmpeg -v warning -ss "$start_at" -to "$end_at" -i "$1" -vf "fps=$fps,scale=$scale:flags=lanczos,palettegen" /tmp/palette.png

# Generate gif
ffmpeg -v warning -ss "$start_at" -to "$end_at" -i "$1" -i /tmp/palette.png -lavfi "fps=$fps,scale=$scale:flags=lanczos[x];[x][1:v]paletteuse" "$2"

rm /tmp/palette.png
