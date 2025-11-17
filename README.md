# Trixie the Timer 💕

A customizable timer with multi-track audio, light and dark themes, and .

## Features

- **Customizable duration**: Set timer duration to 1+ minutes in whole numbers (default 6)
- **Repeat cycles**: Set cycles; auto-repeat for 0+ minutes/hours in whole numbers (rounds number of cycles up to nearest multiple)
- **Themes**: Bubblegum (light) and Candy Raver (dark) with pink/turquoise/cyan palettes
- **Multi-track audio**: Upload 5 tracks via browser interface in addition to the default "Track 1"
- **localStorage persistence**: Uploaded tracks save between sessions
- **Track management**: Delete tracks with minus button
- **Duplicate detection**: Themed popup prevents adding same file twice
- **File size limit**: 10MB per track with validation
- **Loading indicator**: Shows upload progress
- **Test sound**: Preview tracks with test button
- **Visual warnings**: Turquoise at 10s, pulsing pink at 0s
- **Cycle tracking**: Shows current cycle number

## Setup

1. Open `timer.html` in browser
2. Click "+ Add Track" to upload audio files
3. Supported formats: m4a, mp3, wav

## Usage

1. Set timer duration
2. Optional: Set repeat hours/minutes for multiple cycles
3. Click "+ Add Track" to upload songs (saves to localStorage)
4. Select track from buttons
5. Click Start
6. Toggle theme (top-right button)

## Track Management

- **Add**: Click "+ Add Track" button, select audio file
- **Delete**: Click minus sign (−)
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
