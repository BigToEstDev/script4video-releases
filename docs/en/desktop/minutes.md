# **Minutes**
### **Calculate minutes**
When the user clicks the create video button
There are checks of settings, then those resources that fall under the criteria
The calculation of the potentially maximum length of all created videos is performed
When the potential length of the videos is known, the user has reserved potentially used minutes, they are visually written off the balance at the beginning of video generation

At the end of video generation (success, cancellation), minutes from the reserved ones become written off (spent), writing off occurs only for the created videos
**Success** - all videos were created, the generation process was not canceled
**Cancel** - video generation was interrupted, minutes will be charged only for created aideos

The video that was in process of being canceled will not be created and the video file will be deleted

### **Sample Screen-Based Consumption (Audio History)**
On the audio history screen, the minutes are calculated as follows
1 minute (token) - in 1 minute of created video
Video length is calculated based on the length of the audio track
If the adio track is 6 minutes 45 seconds, the minutes will be written off in 6 minutes of the finished video
(rounding in favor of the user)

If there are 12 audio tracks in the directory, 6 meet the criteria for creation, the potential consumption of tokens will be
sum of lengths of 6 audio tracks. Let's say each audio track is 7 minutes long.
When you click on the create video button, the user will have 42 tokens reserved
Upon completion of ALL videos, reserved minutes will be considered spent
When canceled, only the number of tokens will be written off, how many full videos were made before cancellation
0 video was made - 42 tokens return to user account
3 videos were made - 21 tokens will be written off, 21 will be returned to the user, etc.

### **Error Handling**
If a network intranet fails during video creation and generation completes without a network (cancel, success)
In this case, information about the created videos is stored on the device
At the next launch, the application will send information about the operation performed to the service and the minutes will be calculated according to the created videos (charge only for the created videos, return for videos that were not created)
Until then, minutes will remain reserved (until the status of the operation)
If the status of the operation has not arrived within 2 days, the reserved minutes will be written off in full
To send the status of the operation, it is enough to launch the application (if the Internet is available) within 2 days from the date of the operation

### **Calculate consumption for each screen**
**Audio Stories**
1 minute (token) for 1 minute of created video
The calculation is based on the length of the audio track, on the basis of which the video will be created
If the audio is not divisible by full minute, it will be rounded to the least whole number of minutes

**Shorts Split**
2 minutes (tokens) for 10 seconds of created short
The calculation is based on the length of the video track (not reactions videos), on the basis of which the video will be created
If the audio recording is not divisible by 10 seconds, it will be rounded to the nearest whole number of 10 seconds chunk
