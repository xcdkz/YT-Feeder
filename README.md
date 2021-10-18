- [IMPORTANT](#org2e0089f)
- [Introduction](#orgb44430d)
- [Usage](#org1c4a6d5)
  - [Worth noting](#org4a7c8ef)
- [Configuration](#orgd0bd3ca)
- [Requirements](#orgb2809ef)
- [TODO](#orgc55cbc6)


<a id="org2e0089f"></a>

# IMPORTANT

There is an issue with bots &ldquo;advertising&rdquo; this project to random people on Discord, asking for stars and offering free Discord Nitro in exchange. I don&rsquo;t know who these people are and why they are doing that, but if you expect any kind of reward for starring my project, please don&rsquo;t do it. Having said that, I hope you enjoy my using my script 🙂


<a id="orgb44430d"></a>

# Introduction

[YT-Feeder](https://youtu.be/GoCMYeCHMbQ) is a Rofi-Based RSS Reader made specifically for YouTube video platform. It&rsquo;s written purely in bash and allows user to watch or download new videos.


<a id="org1c4a6d5"></a>

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


<a id="org4a7c8ef"></a>

## Worth noting

The default directory for downloaded videos is ~/Videos/


<a id="orgd0bd3ca"></a>

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


<a id="orgb2809ef"></a>

# Requirements

Currently only requirements are:

-   mpv
-   youtube-dl
-   rofi


<a id="orgc55cbc6"></a>

# TODO

-   [ ] Add information about the number of new videos
-   [X] Clean bash code
-   [X] Add option to change the default directory of downloaded videos
-   [X] Add option to play video in the background
-   [X] Add an ability to just use channel&rsquo;s ID in the config file
-   [X] Add option to use a custom script on selected video
