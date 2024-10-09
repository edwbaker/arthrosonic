# arthrosonic <img src="imgs/logo.png" align="right" height="138" alt="arthosonic logo" />

Arthrosonic is a sound segmenter used to prepare files as part of the [FlyTunes](https://www.zooniverse.org/projects/nhmcommunityscience/flytunes) project.

The script takes a directory of sound files (of any type that can be read by `ffmpeg`) and cuts them into segments of length `duration` (seconds) using `sox`, optionally offsetting from the front by `trim` seconds. The files are outputted in mp3 format regardless of input format. A mainfest file is generated listing the files created with metadata that is suitable for uploading via the Zooniverse CLI.

## Installation

### Requirements

- Unix-like operating system.

- sox

- ffmpeg

For details on installing sox and ffmpeg on macOS see details at the start of [Linux audio recipes](https://ebaker.me.uk/notes/linux-audio-recipes.html).

### Install from GitHub

````bash
wget https://raw.githubusercontent.com/edwbaker/arthrosonic/refs/heads/main/arthrosonic
chmod +x arthrosonic
mv arthrosonic /usr/local/bin/
````

## Usage

arthrosonic -i input_directory -o output_directory [-d duration] [-t trim] [-m manifest]

### Options

-i: Input directory containing audio files.

-o: Output directory to store segmented audio files.

-d: Duration of each segment in seconds. Default is 6 seconds.

-m: Generate manifest file. 0 for false, 1 for true. Default is 1.

-t: Offset the start of first segment by this amount in seconds. Default is 0.

-h: Display  help message.

## Etymology

The project name is derived from:

- arthro- (jointed) referencing the segmentation and the fossil myriapod _Arthropleura_.

- sonic referecing sound.

## Notes

This script combines audio manipulations from ffmpeg and sox as described in [Linux audio recipes](https://ebaker.me.uk/notes/linux-audio-recipes.html).

## Support

This script was developed as part of the Urban Nature Project at the [Natural History Museum](https://www.nhm.ac.uk).
