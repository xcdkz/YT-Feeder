- [Gallery](#orgf4c80ad)
- [Introduction](#orgeb0640e)
- [Usage](#org1bcfc1b)
  - [Worth noting](#org4e07348)
- [Configuration](#org03ff352)
- [Requirements](#org9dce189)
- [TODO](#orgf91421a)


<a id="orgf4c80ad"></a>

# Gallery

<p align="center">
  <img src="./assets/yt-feeder-1.png" width="700">
  <img src="./assets/yt-feeder-2.png" width="700">
  <img src="./assets/yt-feeder-3.png" width="700">
</p>

<a id="orgeb0640e"></a>

# Introduction

YT-Feeder is a Rofi-Based RSS Reader made specifically for YouTube video platform. It&rsquo;s written purely in bash and allows user to watch or download new videos.


<a id="org1bcfc1b"></a>

# Usage

While in the project folder:

```bash
chmod +x YT-Feeder
```

Then to actually run the script:

```bash
rofi -show YT-Feeder -modi "YT-Feeder:/Absolute/Path/To/YT-Feeder"
```

I highly suggest binding the above command to your keyboard shortcut of choice. After launch you can select your favorite channel from the list, then select video and then you have a choice to:

-   watch(best) -> watch it in the best quality
-   watch(worst) -> watch it in the worst quality
-   play in the background -> play audio from video in the background
-   open in a web browser -> opens YouTube link in a default web browser
-   download -> download video
-   download audio -> download audio from video
-   command -> use your custom command on video&rsquo;s link

There&rsquo;s also an option to refresh the RSS feeds at the top of the list and there might be an option to stop currently playing audio in the background(only after selecting &ldquo;play in the background&rdquo;).


<a id="org4e07348"></a>

## Worth noting

The default directory for downloaded videos is ~/Videos/ and the default directory for downloaded audio is ~/Music/.


<a id="org03ff352"></a>

# Configuration

Change ~/.config/yt-feeder/config file to configure this script. If it doesn&rsquo;t exist, create it. The general syntax for this file is:

```
// Some comment
rss link or channel's ID
rss link or channel's ID
rss link or channel's ID
DOWNLOAD|~/Videos/folder_for_yt_videos
COMMAND|my_custom_command
DOWNLOAD_AUDIO|~/Music/folder_for_yt_audio
```

Comments must be placed on separate lines, every line starting with &ldquo;//&rdquo; will be ignored by the script

-   `DOWNLOAD` specifies the custom directory where you wish to download your videos.
-   `COMMAND` specifies your custom command to use on youtube links.
-   `DOWNLOAD_AUDIO` specifies the custom directory where you wish to download your audio.


<a id="org9dce189"></a>

# Requirements

Currently only requirements are:

-   mpv
-   youtube-dl
-   ffmpeg
-   rofi


<a id="orgf91421a"></a>

# TODO

-   [X] Add option to open link in the browser
-   [X] Add information about the number of new videos
-   [X] Auto-detect Channel&rsquo;s name from RSS Feed
-   [X] Clean bash code
-   [X] Add option to change the default directory of downloaded videos
-   [X] Add option to play video in the background
-   [X] Add an ability to just use channel&rsquo;s ID in the config file
-   [X] Add option to use a custom script on selected video
