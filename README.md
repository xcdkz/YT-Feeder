- [IMPORTANT](#org80fa9a3)
- [Introduction](#org4020876)
- [Usage](#orgb59721c)
  - [Worth noting](#orgccc62f2)
- [Configuration](#org31acf81)
- [Requirements](#org2dba0af)
- [TODO](#org520b3df)


<a id="org80fa9a3"></a>

# IMPORTANT

There is an issue with bots &ldquo;advertising&rdquo; this project to random people on Discord, asking for stars and offering free Discord Nitro in exchange. I don&rsquo;t know who these people are and why they are doing that, but if you expect any kind of reward for giving a star my project, please don&rsquo;t do it. Having said that, I hope you enjoy using my script 🙂


<a id="org4020876"></a>

# Introduction

**[YT-Feeder Example Video](https://youtu.be/GoCMYeCHMbQ)**

YT-Feeder is a Rofi-Based RSS Reader made specifically for YouTube video platform. It&rsquo;s written purely in bash and allows user to watch or download new videos.


<a id="orgb59721c"></a>

# Usage

While in the project folder:

```bash
chmod +x YT-Feeder
```

Then to actually run the script:

```bash
rofi -show YT-Feeder -modi "YT-Feeder:Absolute/Path/To/YT-Feeder"
```

I highly suggest binding the above command to your keyboard shortcut of choice. After launch you can select your favorite channel from the list, then select video and then you have a choice to:

-   watch(best) -> watch it in the best quality
-   watch(worst) -> watch it in the worst quality
-   play in the background -> play audio from video in the background
-   download -> download the video
-   command -> use your custom command on the video&rsquo;s link

There&rsquo;s also an option to refresh the RSS feeds at the top of the list and there might be an option to stop currently playing audio in the background(only after selecting &ldquo;play in the background&rdquo;).


<a id="orgccc62f2"></a>

## Worth noting

The default directory for downloaded videos is ~/Videos/


<a id="org31acf81"></a>

# Configuration

Change ~/.config/yt-feeder/config file to configure this script. If it doesn&rsquo;t exist, create it. The general syntax for this file is:

```
rss link or channel's ID|channel's name
rss link or channel's ID|channel's name
rss link or channel's ID|channel's name
DOWNLOAD|~/Videos/folder_for_yt_videos
COMMAND|my_custom_command
```

DOWNLOAD and COMMAND lines **must** be at the end of the config file if you wish to use them. DOWNLOAD specifies the custom directory where you wish to download your videos. COMMAND specifies your custom command to use on youtube links.


<a id="org2dba0af"></a>

# Requirements

Currently only requirements are:

-   mpv
-   youtube-dl
-   rofi


<a id="org520b3df"></a>

# TODO

-   [ ] Add information about the number of new videos
-   [X] Clean bash code
-   [X] Add option to change the default directory of downloaded videos
-   [X] Add option to play video in the background
-   [X] Add an ability to just use channel&rsquo;s ID in the config file
-   [X] Add option to use a custom script on selected video
