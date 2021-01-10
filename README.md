# split-video

split-video is a utility that allows you to split a video file into a number of fixed length parts. No re-encoding of the video takes place so the quality of the generated video parts is the same as the original.

**Note**: `ffmpeg` is required in order for the program to function.

## Usage

```
-h, --help            Show help message and exit
-v, --verbose         Turn on debug messages
-i INPUT, --input INPUT
                      Input video
-d DURATION, --duration DURATION
                      How long each part should be in seconds
-f, --force           Remove existing output files if they already exist
```

## Example:

```
./split-video -i large-video.mp4 -f -d 3600
```

The above example will split the file file `large-video.mp4` into separate video files which will be one hour (3,600s) in length.

Each part will be named: large-video-part*x*.mp4 where *x* is in the range 1 to the total number of parts.
