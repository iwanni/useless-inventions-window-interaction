# Dragon Ball Z Window Interaction

![Result Demo](assets/result.gif)

A fun interactive web application where two browser windows containing Goku can "interact" with each other based on their distance. When the windows get close, Goku powers up and fires his Kamehameha wave!

## Features

- **Window Detection**: Automatically detects other browser windows using BroadcastChannel API
- **Distance-based Interaction**: Goku changes animation and audio based on proximity between windows
- **Dynamic Rotation**: Goku rotates to face the other window
- **Immersive Audio**: Different Dragon Ball Z sound effects for charging and firing
- **Mirrored Windows**: Second window shows a flipped version for realistic interaction

## How to Use

1. Open `index.html` in your browser
2. Duplicate the tab or open the same file in a new window
3. For the second window, add `?w=2` to the URL to mirror Goku
4. Move the windows around your screen
5. Watch as Goku powers up and fires his Kamehameha when windows get close!
6. Click or tap on either window to unlock audio (browser requirement)

## URL Parameters

- `?w=1` - Default Goku (faces right)
- `?w=2` - Mirrored Goku (faces left)

## Technical Details

- **Distance Threshold**: 510 pixels between window centers
- **Update Frequency**: 100ms for smooth interaction
- **Audio System**: Sequential audio playback (charge → fire → beam)
- **Browser APIs**: Uses BroadcastChannel for cross-window communication
- **Audio Unlock**: Supports touch, click, and keyboard interaction for audio unlock

## Assets

The project includes Dragon Ball Z themed assets:
- Goku Super Saiyan GIF (normal state)
- Goku Kamehameha GIF (close state)  
- Kamehameha charge sound effect
- Beam firing sound effect
- Continuous beam sound effect

## Live Demo

Simply open `index.html` in two browser windows and experience the magic of window-to-window Kamehameha battles!
