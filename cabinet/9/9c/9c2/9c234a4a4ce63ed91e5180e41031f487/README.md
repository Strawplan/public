# Converting Video to Audio

This script will convert mp4 files to mp3 using `ffmpeg`. Either one specific file or a folder path must be passed as a parameter.

```
#!

# Convert mp4s to mp3s

mp3 () (
    ffmpeg -hide_banner -nostdin -y \
        -i "${1}" -vn "${1}.mp3"
)

if [[ $(file --brief "$1") == "directory" ]]
    then
        find "$1" -name "*.mp4" | while read -r source
            do mp3 "${source}"
        done
    else
        mp3 "${1}"
fi
```

