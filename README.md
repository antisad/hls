# hls_downloader

A posix compliant highly fast and efficient Asynchronous stable m3u8 links parallel downloader that uses shell jobs for controlling parallel download...

```
Usage:
    hls [ -o <filename> ] [ -r | -f ] [ <m3u8_link> ]
    hls -h

Options:
    -h show helptext
    -o filename (default : video)
    -r select highest resolution automatically
    -f skip ffmpeg file conversion (used to enable the video file to run on any video player)
```

# Increase/Decrease Parallel Downloads..

Currently its set to 36 in [line 23](https://github.com/CoolnsX/hls_downloader/blob/main/hls#L23) in script
You can Increase/Decrease it by using ```-n <no. of connections>```

```
Internet Speed = 12 MByte per seconds..
36 (Internet Speed * 3)..
```
NOTE :- Increasing the number will make the download faster but less stable and Decreasing the number will make download slower but stable.. Decrease the number if the script is hanging out during download process..

# Dependency

- ffmpeg for conversion
- openssl for decrypting streams
