# Punk Platformer — Spec

## 1. Project Overview
- **Type**: 2D side-scrolling platformer (single HTML file)
- **Core**: Collect items, avoid enemies, reach the goal
- **Character**: Pixel-art punk with spiky hair

## 2. Visual & Rendering
- **Canvas**: Dynamic resolution (default 1920x1080, selectable: 1280x720, 1366x768, 1600x900, 1920x1080, 2560x1440), pixel-art aesthetic
- **Camera**: Follows player horizontally, fixed vertical
- **Background**: Dark city skyline (parallax)
- **Character size**: ~32x48 px

## 3. Player Character (Punk)
- **Appearance**: Black jacket, neon green/pink mohawk, boots
- **Animations**: Idle (breathing), Run (4 frames), Jump
- **Controls**:
  - Arrow Left/Right or A/D — move
  - Space/Up/W — jump
- **Physics**:
  - Gravity: 0.5
  - Jump force: -12
  - Speed: 5
  - Max fall speed: 10

## 4. World & Platforms
- Tile-based (32x32 tiles)
- Platforms: brick/stone texture (procedurally drawn)
- Ground at bottom, floating platforms above
- Level width: ~2500px (scrolling)

## 5. Collectibles & Enemies
- **Coins**: Yellow circles with sparkle, +10 points
- **Enemy (Angry Robot)**: Patrols left-right on platforms, dies on stomp
- **Goal Flag**: At end of level, triggers win screen

## 6. Game States
- **Start Screen**: Title + "Press Space to Start"
- **Playing**: Main game loop
- **Win**: "YOU WIN!" + score
- **Game Over**: Falling off screen → restart

## 7. UI
- Score display (top-left)
- Lives: 3 hearts (top-right)
- Pixel font (monospace fallback)

## 8. Audio
- Simple Web Audio API beeps for: jump, coin, enemy kill, win