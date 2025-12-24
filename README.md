# SnakeMove 🐍👆

A webcam-controlled Snake game where you control the snake using finger gestures! Designed with accessibility in mind, featuring adjustable difficulty settings for players of all ages and skill levels.

## Features

### Gesture Control
- **Point your index finger** to move the snake (up/down/left/right)
- **Close your fist** to stop the snake
- Real-time hand tracking using MediaPipe
- No keyboard required - fully hands-free gameplay!

### Customizable Difficulty Settings

#### 🎯 Board Size (10x10 to 30x30)
- **Small boards (10x10)**: Quick games, tighter spaces
- **Default (20x20)**: Balanced gameplay
- **Large boards (30x30)**: More room to maneuver, longer games

#### ⚡ Snake Speed
- **Slow (0.5x)**: Perfect for beginners and elderly users
- **Normal (1x)**: Default comfortable speed
- **Fast (2x)**: Challenge mode for experienced players

#### 🎯 Moving Food
- **Stationary**: Classic snake gameplay
- **Slow (moves every 3 seconds)**: Gentle challenge
- **Fast (moves every 1 second)**: Dynamic target for advanced players
- Food moves one step at a time to neighboring positions

### Accessible Design
- Slower default speed compared to traditional snake games
- Deliberate control - snake only moves when actively pointing
- Stop anytime by closing your hand
- Clear visual feedback showing detected gestures
- Adjustable settings for different skill levels

## How to Play

### Setup
1. Download `index.html`
2. Open it in a modern browser (Chrome, Firefox, or Edge recommended)
3. Allow camera permissions when prompted

### Gameplay
1. Click **"Start Camera"** - Position your hand clearly in front of the webcam
2. Adjust difficulty sliders to your preference
3. Click **"Start Game"**
4. Point your index finger to control the snake:
   - 👆 Point UP - Snake moves up
   - 👇 Point DOWN - Snake moves down
   - 👈 Point LEFT - Snake moves left
   - 👉 Point RIGHT - Snake moves right
   - ✊ Close fist - Snake stops
5. Eat the red food to grow and score points!

### Tips
- Hold your hand clearly visible to the camera
- Point with **only your index finger** extended
- Good lighting improves hand detection
- The snake only moves when you're actively pointing

## Technology Stack

- **HTML5 Canvas** - Game rendering
- **MediaPipe Hands (Google)** - Real-time hand tracking
- **Vanilla JavaScript** - Game logic
- **Webcam API** - Camera access

## Browser Requirements

- Modern browser with webcam support
- Camera permissions enabled
- Recommended: Chrome 90+, Firefox 88+, or Edge 90+

## Adjusting Game Parameters

The code is organized with clear section markers for easy customization:

### Speed Adjustment
```javascript
// ===== SPEED CONTROL VARIABLES =====
const BASE_SPEED = 300; // Default game speed in milliseconds
```

### Food Movement Timing
```javascript
// ===== MOVING FOOD CONTROL =====
// In updateFoodSpeed() function:
foodMovementInterval = 3000; // Slow: 3 seconds
foodMovementInterval = 1000; // Fast: 1 second
```

### Board Size Range
```html
<!-- Board Size Slider -->
<input type="range" id="gridSlider" min="10" max="30" value="20">
```

## Game Mechanics

- **Starting Length**: Snake begins with 3 segments
- **Score**: +10 points per food eaten
- **Growth**: Snake grows by 1 segment per food
- **Game Over**: Hitting walls or yourself ends the game
- **Movement**: Snake only moves when finger is pointing (deliberate control)

## Future Enhancement Ideas

- Multiple difficulty presets
- Sound effects
- High score tracking
- Different food types with various effects
- Obstacles and power-ups
- Multiplayer mode with two hands

## Author
- Mario Nascimento (nascimento.mario@gmail.com) with extensive help from Claude (Anthropic)

## License

MIT

## Credits

Created for accessibility and fun - perfect for elderly users, children, and anyone who enjoys hands-free gaming!

Hand tracking powered by [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) by Google.
