```
ffmpeg -i asset -c:v libx264
```

`-c` is for codec

The codec must refer to a specific stream

| Specifier | Meaning     | Example        |
| --------- | ----------- | -------------- |
| `:v`      | video       | `-c:v libx264` |
| `:a`      | audio       | `-c:a aac`     |
| `:s`      | subtitles   | `-c:s copy`    |
| `:d`      | data        | rare           |
| `:t`      | attachments | fonts in MKV   |

Since an input can have multiple streams. For example:

```
  Stream #0:0(und): Audio: aac (LC) (mp4a / 0x6134706D), 44100 Hz, stereo, fltp, 125 kb/s (default)
  
  Stream #0:1(und): Video: h264 (High) (avc1 / 0x31637661), yuv420p, 1280x720 [SAR 1:1 DAR 16:9], 1991 kb/s, 24 fps, 24 tbr, 24k tbn, 48 tbc (default)
```