# Dragon Ball Z - Goku Kamehameha Window Interaction

Demo
- [Default Goku](https://iwanni.github.io/useless-inventions-window-interaction?w=1) - `?w=1` (faces right)
- [Mirrored Goku](https://iwanni.github.io/useless-inventions-window-interaction?w=2) - `?w=2` (faces left)

![Result Demo](assets/result.gif)

A fun interactive web application where two browser windows containing Goku and Vegeta can "interact" with each other based on their distance. When the windows get close, they power up and fire their signature attacks!

## Features

- **Window Detection**: Automatically detects other browser windows using BroadcastChannel API
- **Distance-based Interaction**: Goku changes animation and audio based on proximity between windows
- **Dynamic Rotation**: Goku rotates to face the other window
- **Immersive Audio**: Different Dragon Ball Z sound effects for charging and firing
- **Character Selection**: Choose between Goku (?w=1) and Vegeta (?w=2) for epic battles

## How to Use

1. Open `index.html` in your browser
2. Duplicate the tab or open the same file in a new window
3. For the second window, add `?w=2` to the URL to use Vegeta
4. Move the windows around your screen
5. Watch as the characters power up and fire their attacks when windows get close!
6. Click or tap on either window to unlock audio (browser requirement)

## URL Parameters

- [Goku](https://iwanni.github.io/useless-inventions-window-interaction?w=1) - `?w=1` (default character)
- [Vegeta](https://iwanni.github.io/useless-inventions-window-interaction?w=2) - `?w=2` (rival character)

## Technical Details

- **Distance Threshold**: 510 pixels between window centers
- **Update Frequency**: 100ms for smooth interaction
- **Audio System**: Sequential audio playback (charge → fire → beam)
- **Browser APIs**: Uses BroadcastChannel for cross-window communication
- **Audio Unlock**: Supports touch, click, and keyboard interaction for audio unlock

## How BroadcastChannel API Works

![BroadcastChannel Diagram](broadcast-channel-diagram.html)

The application uses the BroadcastChannel API to enable real-time communication between browser windows:

1. **Broadcasting**: Each window broadcasts its position (x, y, width, height) every 100ms
2. **Listening**: All windows listen for messages from other windows on the same channel
3. **Distance Calculation**: When receiving another window's position, calculate the distance between window centers
4. **Visual Effects**: Trigger character animations and audio effects when windows are close (< 510px apart)

[View Interactive Diagram](broadcast-channel-diagram.html)

## Assets

The project includes Dragon Ball Z themed assets:
- Goku Super Saiyan GIF and Kamehameha attack
- Vegeta GIF and Kamehameha attack
- Dragon Ball Z sound effects (charge, fire, beam)
- Character-specific animations and audio

## Live Demo

Simply open `index.html` in two browser windows and experience the epic Goku vs Vegeta window battles!

## Credits

- **Sound Effects**: [MyInstants](https://www.myinstants.com/)
- **GIF Images**: 
  - [Super Saiyan Goku](https://tenor.com/view/super-saiyan-goku-dbz-charging-gif-17464307) - Tenor
  - [Goku Kamehameha](https://tenor.com/view/goku-dragonball-gif-8466428) - Tenor
  - [Vegeta](https://tenor.com/view/vegeta-gif-1615384944259328642) - Tenor
  - [Vegeta Additional](https://gifgifs.com/anime/dragon-ball-z/32161-vegeta-vegeta-14.html) - GifGifs
  - [Vegeta Kamehameha](https://gifs.alphacoders.com/gifs/view/35158) - Alpha Coders
