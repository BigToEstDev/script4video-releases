# **Audio Stories**
Audio story feed opens from the app's homepage
It is designed to create an audio history video format
Pictures and optional subtitles are shown against the background of the audio track

The basis for creating video is audio tracks
Videos are created in **horizontal** 16:9 format

### **Directories**
There are 4 sections to work with this screen:
* Directory with audio - from here all audio will be taken to create video
* Directory with images - from here all images will be taken to create a video
* Diretory with subtitles - when creating a video, it is assumed that the video will be without subtitles. If no directory is selected, no subtitles will be added. Subtitles are supported in .SRT format. To add subtitles to a video, the subtitle file must have the same **name** as the audio file to which it will be applied. Example - the name of the audio audio_1, the name of the subtitle file should be audio_1
* Save directory - all ready-made videos will be saved to this directory, it must be unique and not coincide with other directories
* Directory for generated idios - this directory contains audio for which videos have been generated. This is to avoid re-generating video from already used audio.

### **Video Settings**
In the upper panel of the screen there is a video settings icon
The following settings are presented in the video settings:
* Maximum Number of Videos - the maximum number of videos that will be created in 1 create call, regardless of the number of audio tracks in the folder
* Minimum audio track length - all tracks shorter than this number will be ignored when creating video
* Maximum audio track length - all tracks larger than this number will be ignored when creating video
* Picture display time - how long will the picture be displayed on the final video, after this time the image will change
* Filter not 16:9 images - if in the directory for images there are images of the format not only 16:9, then with this setting enabled, such images will be filtered, with the setting disabled, all images from the directory will be allowed to create video. If the picture format is 2:3 (example), the picture will be entered in the 16:9 format - black edges will appear on the sides of the video when showing such a picture

### **Displaying pictures in preview**
When creating a video, pictures are selected in a random order, if there is only 1 picture in the directory that fits the selected parameters, only it will be shown throughout the video.

Displaying pictures in preview - pictures are loaded automatically. You can see which pictures will be used in the video, for this there are arrows on the sides of the preview for scrolling through the pictures.

### **Display Preview subtitles and edit subtitles**
In the upper panel of the screen there is an icon for setting the appearance of subtitles for video
The following subtitle customization mechanisms are presented:
* Font selection - 8 fonts available
* Font size
* Font boldness
* Capitalize only
* Text Color Selection
* Select text stroke color
* Text stroke thickness if 0 - no stroke
* Blur text strokes

All customization of subtitles will be displayed in the preview.

### **Apply subtitles to videos**
When creating a video, it is assumed that the video will be without subtitles. If no directory is selected, no subtitles will be added. Subtitles are supported in .SRT format. To add subtitles to a video, the subtitle file must have the same **name** as the audio file to which it will be applied. Example - the name of the audio audio_1, the name of the subtitle file must be audio_1.

External video subtitle settings will be applied to **all** videos created in one cycle

### **Calculation and Token Consumption**
On the audio history screen, the minutes are calculated as follows
1 minute (token) - in 1 minute of created video
Video length is calculated based on the length of the audio track
If the adio track is 6 minutes 45 seconds, minutes (tokens) will be written off in 6 minutes of the finished video
(rounding in favor of the user)

If there are 12 audio tracks in the directory, 6 meet the criteria for creation, the potential consumption of tokens will be the sum of the lengths of 6 audio tracks. Let's say each audio track is 7 minutes long.
When you click on the create video button, the user will have 42 tokens reserved
At the end of ALL video creation, reserved minutes (tokens) will be considered spent
When canceled, only the number of tokens will be written off, how many full videos were made before cancellation
0 video was made - 42 tokens return to user account
3 videos were made - 21 tokens will be written off, 21 will be returned to the user, etc.

### **Save Settings**
All settings and parameters are automatically saved in the folder
.script4video in settings.json under audio stories

### **Save Video**
* Video saved in audio title + creation time format