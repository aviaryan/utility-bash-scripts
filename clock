#!/bin/bash
#
# Usage:
#    clock list        # list available timezones
#    clock TIMEZONE    # using one of the available timezones

if [ $# != 1 ]; then
    echo Usage:
    echo $0 list
    echo or
    echo $0 TIMEZONE
    exit 2
fi

unameOut=$(uname -s)
case "${unameOut}" in
  Linux*)  machine=Linux;;
  Darwin*) machine=Mac;;
  *)       echo "${unameOut} is not supported"; exit 1
esac

if [ $1 == "list" ]; then
  case "${unameOut}" in
    Linux*)  timedatectl list-timezones; exit 0;;
    Darwin*) sudo systemsetup -listtimezones | less; exit 0;;
  esac
fi

case "${unameOut}" in
  Linux*)  TZ_LIST=$(timedatectl list-timezones --no-pager);;
  Darwin*) TZ_LIST=$(sudo systemsetup -listtimezones);;
esac

if [[ $TZ_LIST == *"$1"* ]]; then
    TZ=$1 date
    exit 0
fi

echo Invalid timezone specified!
echo Please use "$0 list" to see what timezones are available.
exit 1
