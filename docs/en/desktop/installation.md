# Installation Guide

## First Launch

When you first open script4video, the app will check for required dependencies (FFmpeg). If FFmpeg is not installed, you will see a download dialog.

Click **"Download FFmpeg"** and wait for the download to complete. This usually takes 1-2 minutes depending on your internet connection.

## Manual Installation

If the automatic download fails, you can install FFmpeg manually.

### Step 1: Download FFmpeg

Download FFmpeg for your platform:

| Platform | Download Link |
|----------|---------------|
| Windows | [ffmpeg-release-essentials.zip](https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip) |
| macOS | [ffmpeg.zip](https://evermeet.cx/ffmpeg/) |
| Linux | [ffmpeg-release-amd64-static.tar.xz](https://johnvansickle.com/ffmpeg/releases/ffmpeg-release-amd64-static.tar.xz) |

### Step 2: Find the Installation Folder

Open the folder where script4video stores its data:

| Platform | Folder Path |
|----------|-------------|
| Windows | `C:\Users\<YourName>\.script4video\bin\` |
| macOS | `/Users/<YourName>/.script4video/bin/` |
| Linux | `/home/<YourName>/.script4video/bin/` |

If the `bin` folder doesn't exist, create it.

### Step 3: Extract and Copy Files

Extract the downloaded archive and copy the following files to the `bin` folder:

**Windows:**
```
ffmpeg.exe
ffprobe.exe
```

**macOS / Linux:**
```
ffmpeg
ffprobe
```

### Step 4: Restart the App

Close and reopen script4video. The app should now detect FFmpeg and work correctly.

## Troubleshooting

### "FFmpeg not found" after manual installation

- Check that files are named exactly `ffmpeg.exe` and `ffprobe.exe` (Windows) or `ffmpeg` and `ffprobe` (macOS/Linux)
- Make sure files are in the `bin` folder, not a subfolder
- On macOS/Linux: ensure files have execute permission (`chmod +x ffmpeg ffprobe`)

### Download fails or freezes

- Check your internet connection
- Try downloading manually (see above)
- Temporarily disable firewall/antivirus and retry

### "FFmpeg failed to execute"

- The downloaded file may be corrupted. Delete it and try again
- On macOS: you may need to allow the app in System Preferences > Security & Privacy
- On Windows: you may need to unblock the file (Right-click > Properties > Unblock)

## Reinstalling the App

When you reinstall or update script4video:

- Your FFmpeg installation is preserved
- Your settings are preserved
- No need to download FFmpeg again

## Completely Removing the App

To completely remove script4video and all its data:

1. Uninstall the app normally
2. Delete the `.script4video` folder from your home directory

## Need Help?

If you're still having issues, contact support with:

- Your operating system (Windows/macOS/Linux)
- The error message you see
- Screenshots if possible
