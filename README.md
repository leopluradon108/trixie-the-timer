# Trixie the Timer 💕

Optimized break timer with dual themes, multi-track audio, and localStorage persistence.

## Features

- **Customizable duration**: 1-999 minutes (default 6)
- **Repeat cycles**: Auto-repeat for set hours/minutes (rounds to nearest multiple)
- **Dual themes**: Bubblegum (light) and Candy Raver (dark) with pink/turquoise/cyan palettes
- **Multi-track audio**: Upload unlimited tracks via browser interface
- **localStorage persistence**: Uploaded tracks saved between sessions
- **Track management**: Delete tracks with hover button (1.5s delay tooltip)
- **Duplicate detection**: Themed popup prevents adding same file twice
- **File size limit**: 10MB per track with validation
- **Loading indicator**: Shows upload progress
- **Test sound**: Preview tracks with pause/resume (10s auto-reset)
- **Visual warnings**: Turquoise at 10s, pulsing pink at 0s
- **Cycle tracking**: Shows current cycle number

## Setup

1. Open `timer.html` in browser
2. Click "+ Add Track" to upload audio files
3. Supported formats: m4a, mp3, wav, ogg

## Usage

1. Set timer duration
2. Optional: Set repeat hours/minutes for multiple cycles
3. Click "+ Add Track" to upload songs (saves to localStorage)
4. Select track from buttons
5. Click Start
6. Toggle theme (top-right button)

## Track Management

- **Add**: Click "+ Add Track" button, select audio file
- **Delete**: Hover track button for 1.5s, click minus sign (−)
- **Default**: Track 1 (makes-sense.m4a) cannot be deleted
- **Storage**: ~5-10MB localStorage limit (several songs)
- **Duplicates**: Popup warns if filename already exists
- **Size limit**: 10MB per file maximum

## Performance Optimizations

- **Cached DOM elements**: Single query per element
- **Efficient state management**: Centralized state object
- **Selective rendering**: Only rebuilds changed track buttons
- **File validation**: Size check before processing
- **Error handling**: Graceful fallbacks for audio/storage failures
- **Memory cleanup**: Proper audio object disposal

## Technical

- Single HTML file, no dependencies
- No network after initial load
- localStorage for track persistence (base64 encoding)
- Theme persists via CSS classes
- 3s pause between repeat cycles
- Clearing browser data removes uploaded tracks