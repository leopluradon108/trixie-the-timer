# Trixie the Timer 💕

A customizable break timer with dual color themes and audio notifications. Perfect for Pomodoro-style work sessions or regular break reminders.

## Features

- ⏱️ **Customizable Timer Duration** - Set any duration from 1-999 minutes
- 🔄 **Repeat Cycles** - Automatically repeat for specified hours/minutes (rounds up to nearest multiple)
- 🎨 **Dual Themes**
  - **Bubblegum** (light mode) - Pink, white, and turquoise pastels
  - **Candy Raver** (dark mode) - Neon pink, cyan, and dark navy
- 🎵 **Audio Notifications** - Plays custom sound when timer completes
- 🎯 **Visual Warnings** - Timer changes color at 10 seconds (turquoise) and 0 seconds (pulsing pink)
- ⏸️ **Timer Controls** - Start, Stop, Reset, and Test Sound buttons
- 📊 **Cycle Tracking** - Shows current cycle number when using repeat mode

## Setup

### 1. Download Files

Clone or download this repository:
```bash
git clone https://github.com/YOUR-USERNAME/trixie-the-timer.git
cd trixie-the-timer
```

### 2. Add Your Audio File

Place an audio file in the same folder as `break-timer.html` and name it:
```
lofi-beat-by-syd.m4a
```

**Supported formats:**
- `.m4a` (recommended for Safari/Chrome)
- `.mp3` (universal support)
- `.wav` (larger files)

**To use a different audio file:**
1. Open `break-timer.html` in a text editor
2. Find line 3: `const AUDIO_FILE = 'lofi-beat-by-syd.m4a';`
3. Change the filename to match yours: `const AUDIO_FILE = 'your-file.mp3';`

### 3. Run the Timer

Double-click `break-timer.html` to open in your browser. That's it!

## Usage

### Basic Timer
1. Set your desired duration (default: 6 minutes)
2. Click **Start**
3. Take your break when the timer goes off!

### Repeat Mode
Want the timer to repeat for a specific amount of time?
1. Enter total duration in the "Repeat Until" fields
2. Example: Set timer to 6 minutes, repeat until 1 hour = 10 cycles (60 minutes total)
3. The timer auto-restarts after each cycle with a 3-second break

### Theme Toggle
Click the theme button (top-right) to switch between:
- 🌙 **Candy Raver** (dark mode)
- ☀️ **Bubblegum** (light mode)

### Test Sound
Click **Test Sound** to preview your audio without starting the timer.

## Color Palettes

### Bubblegum (Light Mode)
- Pink: `#FFB3D9`, `#FFC9E3`, `#FF69B4`
- White: `#FFFFFF`, `#FFF5F8`
- Turquoise: `#40E0D0`, `#00CED1`
- Text: `#8B4F6F`, `#6B3555`

### Candy Raver (Dark Mode)
- Pink: `#FF69B4`, `#FFB3D9`, `#ff1493`
- Navy: `#1A1A2E`, `#16213E`, `#0F3460`
- Cyan: `#00FFFF`, `#0FF0FC`

## File Structure

```
trixie-the-timer/
├── break-timer.html        # Main timer application
├── lofi-beat-by-syd.m4a   # Your audio file (not tracked by git)
├── .gitignore              # Excludes audio files from git
└── README.md               # This file
```

## Browser Compatibility

- ✅ Chrome/Edge (full support)
- ✅ Safari (full support)
- ✅ Firefox (use .mp3 instead of .m4a)

## Troubleshooting

### Audio doesn't play
1. **Check file location** - Audio file must be in same folder as HTML
2. **Check filename** - Must match exactly (case-sensitive)
3. **Try different format** - Convert m4a to mp3 if browser doesn't support it:
   ```bash
   ffmpeg -i lofi-beat-by-syd.m4a lofi-beat-by-syd.mp3
   ```
4. **Check browser console** - Open DevTools (F12) to see error messages

### Timer doesn't start
- Refresh the page (Ctrl/Cmd + R)
- Clear browser cache
- Try a different browser

## Development

### Adding New Features
The code is organized into clear sections:
- Configuration (line 3)
- State Variables (line 5)
- DOM Elements (line 12)
- Theme Functions (line 25)
- Calculation Functions (line 31)
- Display Functions (line 48)
- Audio Functions (line 61)
- Timer Control Functions (line 76)
- Event Listeners (line 166)

### Customizing Audio Behavior
To change when/how audio plays, edit the `playSound()` function starting at line 61.

## Git Workflow

Audio files are excluded from version control via `.gitignore`. To work on this project:

```bash
# Clone repo (no audio included)
git clone https://github.com/YOUR-USERNAME/trixie-the-timer.git

# Add your own audio file locally
cp /path/to/your-audio.m4a trixie-the-timer/lofi-beat-by-syd.m4a

# Make changes
git add break-timer.html
git commit -m "Your changes"
git push

# Audio file stays on your computer only!
```

## Credits

Timer inspired by Trixie Mattel's iconic pink aesthetic.

## License

MIT License - Feel free to use and modify!