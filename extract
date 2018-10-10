#!/bin/bash

if [ $# -lt 1 ]; then
    echo "Usage: $(basename "$0") file"
    exit 1
fi

if [ -f "$1" ]; then
    case $1 in
        *.tar.xz)   tar -xvf "$1"                         ;;
        *.tar.bz2)  tar -jxvf "$1"                        ;;
        *.tar.gz)   tar -zxvf "$1"                        ;;
        *.bz2)      bunzip2 "$1"                          ;;
        *.dmg)      hdiutil mount "$1"                    ;;
        *.gz)       gunzip "$1"                           ;;
        *.tar)      tar -xvf "$1"                         ;;
        *.tbz2)     tar -jxvf "$1"                        ;;
        *.tgz)      tar -zxvf "$1"                        ;;
        *.zip)      unzip "$1"                            ;;
        *.pax)      cat "$1" | pax -r                     ;;
        *.pax.z)    uncompress "$1" --stdout | pax -r     ;;
        *.rar)      7z x "$1"                             ;;
        *.z)        uncompress "$1"                       ;;
        *.7z)       7z x "$1"                             ;;
        *)          echo "'$1' cannot be extracted/mounted via extract()" ;;
    esac
else
    echo "'$1' is not a valid file"
fi

