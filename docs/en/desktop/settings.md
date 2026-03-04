# Settings
This guide explains all available settings in script4video application.

---

## Settings File Location
All settings are saved automatically and persist between app restarts.

| Platform | Path |
|----------|------|
| Windows | `C:\Users\<username>\AppData\Roaming\.script4video\settings.json` |
| macOS | `~/Library/Application Support/.script4video/settings.json` |
| Linux | `~/.local/share/.script4video/settings.json` |

---

## Global Settings
These settings apply to the entire application.

### Language
**Location**: Main Screen > Gear Icon > Language
Select the interface language for the entire application.

| Option | Description |
|--------|-------------|
| English | English interface |
| Русский | Russian interface |

**Default**: System language (English if system language is not Russian)
**Note**: Language changes apply immediately to all screens and dialogs.

---

### Render Device
**Location**: Main Screen > CPU Icon
Select which processor will be used for video rendering.

| Option | Description |
|--------|-------------|
| CPU | Use the main processor (slower but always available) |
| GPU (name varies) | Use graphics card (faster, recommended) |

**Default**: CPU
**How to choose**:
- If you have a dedicated graphics card (NVIDIA, AMD), select it for faster rendering
- If you only have an integrated GPU (Intel UHD, AMD Radeon Graphics), CPU might be comparable in speed
- You can only select one render device at a time
**Tip**: Open Task Manager during rendering to verify which device is being used.

---

## Account Settings
**Location**: Main Screen > User Icon
View and manage your account information.

| Field | Description |
|-------|-------------|
| Email | Your account email address |
| Device ID | Unique identifier of this device (first 16 characters shown) |
| Minutes | Your available token balance |

### Unlink Device
Removes this device from your account. After unlinking:
- You'll need to link the device again to use the app
- Your minutes remain in your account
- A confirmation dialog appears before unlinking

---

## Audio Stories Settings
Settings specific to the Audio Stories video creation mode.

### Video Settings
**Location**: Audio Stories Screen > Gear Icon

#### Max Video Count
Maximum number of videos to create in one batch.

| Parameter | Value |
|-----------|-------|
| Range | 1 - 100 |
| Default | 10 |

**Example**: If set to 10 and your audio folder has 20 files, only 10 videos will be created.

---

#### Min Audio Duration
Minimum audio file length (in minutes) to be processed.

| Parameter | Value |
|-----------|-------|
| Range | 1 - 60 minutes |
| Default | 1 minute |

Audio files shorter than this value will be skipped.

---

#### Max Audio Duration
Maximum audio file length (in minutes) to be processed.

| Parameter | Value |
|-----------|-------|
| Range | 5 - 60 minutes |
| Default | 60 minutes |

Audio files longer than this value will be skipped.
**Note**: Min Audio Duration must be less than Max Audio Duration. The app automatically adjusts values if needed.

---

#### Image Duration
How long each background image is displayed before switching to the next one.

| Parameter | Value |
|-----------|-------|
| Range | 1 - 5 minutes |
| Default | 3 minutes |

**Example**: If set to 3 minutes and audio is 12 minutes long, the video will cycle through 4 different images.

---

#### Skip Non-16:9 Images
When enabled, images that don't match the 16:9 aspect ratio will not be used.

| Value | Behavior |
|-------|----------|
| Enabled | Only 16:9 images are used |
| Disabled | All images are used (may cause stretching or cropping) |

**Default**: Disabled

---

### Subtitle Settings
**Location**: Audio Stories Screen > "S" Button
Customize how subtitles appear in your videos.

#### Font
Select the font family for subtitles.

| Available Fonts |
|-----------------|
| Arial |
| Times New Roman |
| Verdana |
| Georgia |
| Courier New |
| Impact |
| Comic Sans MS |
| Trebuchet MS |

**Default**: IBM Plex Mono

---

#### Font Size
Size of subtitle text.

| Parameter | Value |
|-----------|-------|
| Range | 8 - 32 |
| Default | 16 |

---

#### Font Weight
Thickness/boldness of subtitle text.

| Parameter | Value |
|-----------|-------|
| Range | 100 - 900 |
| Step | 100 |
| Default | 400 |

| Value | Meaning |
|-------|---------|
| 100-300 | Light |
| 400 | Normal |
| 500-600 | Medium |
| 700-900 | Bold |

---

#### Uppercase
Convert all subtitle text to uppercase letters.

| Value | Behavior |
|-------|----------|
| Enabled | ALL TEXT IN CAPITALS |
| Disabled | Text as written in subtitle file |

**Default**: Enabled

---

#### Text Color
Color of the subtitle text.

| Parameter | Value |
|-----------|-------|
| Format | HEX color (#RRGGBB) |
| Default | #ffffff (white) |

---

#### Border Color
Color of the outline/stroke around subtitle text.

| Parameter | Value |
|-----------|-------|
| Format | HEX color (#RRGGBB) |
| Default | #000000 (black) |

---

#### Border Width
Thickness of the outline around subtitle text.

| Parameter | Value |
|-----------|-------|
| Range | 0 - 10 |
| Default | 1 |

Set to 0 to disable the border completely.

---

#### Border Blur
Apply a soft blur effect to the subtitle border.

| Value | Behavior |
|-------|----------|
| Enabled | Border has a soft, blurred edge |
| Disabled | Border has a sharp edge |

**Default**: Disabled
**Note**: Border Blur is only available when Border Width is greater than 0.

---

## Folder Settings
**Location**: Audio Stories Screen > Left Sidebar
These are working folders selected for each session. They are saved and restored automatically.

| Folder | Purpose |
|--------|---------|
| Upload Audio | Source folder with audio files (MP3, WAV, etc.) |
| Upload Images | Source folder with background images (JPG, PNG, etc.) |
| Upload Subtitles | Source folder with subtitle files (SRT format) |
| Save Folder | Destination folder for generated videos |
| Generated Audio | Folder for processed audio files after generation |

**Important**: Save Folder must be different from all source folders.

---

## Settings Reset
To reset all settings to defaults:

1. Close the application completely
2. Navigate to the settings folder (see paths above)
3. Delete the `settings.json` file
4. Restart the application

All settings will be restored to their default values.
