# **Shorts Split**
Shorts Split screen opens from the app's homepage
It is designed to create split-screen reaction-style videos
The screen combines a main video with a reaction video in a vertical format

The basis for creating video is main videos from the upload folder
Videos are created in **vertical** 9:16 format suitable for YouTube Shorts, TikTok, and Instagram Reels

### **Directories**
There are 4 sections to work with this screen:
* Directory with videos - main content videos that will be used as the primary video source
* Directory with reactions - reaction videos that will be combined with the main video
* Save directory - all ready-made videos will be saved to this directory, it must be unique and not coincide with other directories
* Directory for used videos - after successful generation, source videos are moved here to avoid re-generating videos from already used content

### **Video Customization**
In the options panel there is a Customization tab with the following settings:

**Content Position** - determines the vertical arrangement of videos:
* Video-Reaction - main video appears on top, reaction video on bottom
* Reaction-Video - reaction video appears on top, main video on bottom

**Split Ratio** - controls the screen space distribution between videos:
* 50-50 - both videos take equal space
* 60-40 - main video takes 60%, reaction takes 40%
* 70-30 - main video takes 70%, reaction takes 30%

The split ratio always refers to the main video size regardless of content position.

### **Video Settings**
In the Settings tab you can configure video processing behavior:

**Maximum Video Length** - how to handle videos longer than 3 minutes:
* Skip video - videos longer than 3 minutes will be skipped during generation
* Cut video - videos longer than 3 minutes will be trimmed to 3 minutes

**Minimum Video Length** - all videos shorter than 20 seconds will be ignored when creating videos

**Reaction Policy** - how reaction videos are applied:
* Loop reaction - if the reaction video is shorter than the main video, it will loop to match the duration
* Use different reactions - multiple different reaction clips will be used sequentially to fill the duration

If the reaction video is longer than the main video, it will be trimmed to match the main video duration.

### **Preview**
The preview panel shows how the final video layout will look based on your selected content position and split ratio. Thumbnails from both the videos and reactions folders are displayed in their respective positions.

Click the refresh button next to the preview to reload thumbnails if you've added new videos to the folders.

### **Supported Formats**
The following video formats are supported: MP4, MOV, AVI, MKV, WEBM, WMV, FLV, M4V

### **Calculation and Token Consumption**
On the Shorts Split screen, minutes are calculated as follows:
2 minutes (tokens) for 10 seconds of created short.
The calculation is based on the length of the video track (not reactions videos), on the basis of which the video will be created.

If the audio recording is not divisible by 10 seconds, it will be rounded to the nearest whole number of 10 seconds chunk.
(rounding in favor of the user)

When you click the Generate button, tokens will be reserved based on total expected output duration.
At the end of ALL video creation, reserved minutes (tokens) will be considered spent.
When cancelled, only the number of tokens will be written off for completed videos before cancellation.

### **Save Settings**
All settings and parameters are automatically saved in the folder
.script4video in settings.json under shortsSplit

### **Save Video**
* Videos are saved with the original video title + creation timestamp
