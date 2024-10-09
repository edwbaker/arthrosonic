# arthrosonic <img src="imgs/logo.png" align="right" height="138" alt="arthosonic logo" />

Arthrosonic is a sound segmenter used to prepare files as part of the FlyTunes project.

## Installation

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
