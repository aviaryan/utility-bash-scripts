#!/bin/bash

if [ ! -d ~/Downloads/Videos ]; then
    mkdir -p ~/Downloads/Videos
fi

cd ~/Downloads/Videos || return

if hash aria2c 2> /dev/null; then
  youtube-dl -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best' --merge-output-format mp4 --external-downloader aria2c -o '%(title)s-%(id)s-%(format_id)s.%(ext)s' "$1"
else
  youtube-dl -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best' --merge-output-format mp4 -o '%(title)s-%(id)s-%(format_id)s.%(ext)s' "$1"
fi
