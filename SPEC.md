# Snake Game Specification

## 1. Project Overview
- **Project name**: Snake Game
- **Type**: Browser-based game (HTML/CSS/JS)
- **Core functionality**: Classic snake game with keyboard controls, scoring, and game over detection
- **Target users**: Casual gamers

## 2. UI/UX Specification

### Layout Structure
- Centered game container
- Game canvas (400x400px)
- Score display above canvas
- Game over overlay modal
- Start/Restart button

### Visual Design
- **Color palette**:
  - Background: #0f0f23 (deep dark blue)
  - Game board: #1a1a2e (dark purple-blue)
  - Snake head: #00ff88 (neon green)
  - Snake body: #00cc6a (darker green)
  - Food: #ff3366 (neon pink)
  - Score text: #ffffff
  - Border/grid: #2d2d44
  - Button: #6c5ce7 (purple)
  - Button hover: #a29bfe (light purple)

- **Typography**:
  - Font: 'Orbitron', sans-serif (Google Fonts - futuristic gaming feel)
  - Score: 28px bold
  - Game over text: 48px bold
  - Button: 18px bold

- **Visual effects**:
  - Subtle glow on snake (box-shadow)
  - Pulsing animation on food
  - Grid pattern on game board
  - Smooth transitions on buttons

### Components
- Score panel (displays current score)
- Game canvas with grid
- Start button (initial state)
- Game over overlay with score and restart button

## 3. Functionality Specification

### Core Features
1. **Snake movement**:
   - Snake moves continuously in current direction
   - Speed: 100ms per tick
   - Initial length: 3 segments
   - Initial position: center-left

2. **Controls**:
   - Arrow keys: Up, Down, Left, Right
   - Cannot reverse direction (can't go left if moving right)
   - Initial direction: Right

3. **Food**:
   - Random position on grid (not on snake)
   - One food at a time
   - Eating food: snake grows by 1, score +10

4. **Scoring**:
   - Start at 0
   - +10 per food eaten
   - Display current score

5. **Game over conditions**:
   - Snake hits wall (boundary collision)
   - Snake hits itself (self collision)

6. **Game states**:
   - Ready (before start)
   - Playing
   - Game Over

### Edge Cases
- Prevent 180-degree turns
- Food cannot spawn on snake body
- Handle rapid key presses (queue or ignore)

## 4. Acceptance Criteria
- [ ] Game canvas renders correctly
- [ ] Snake moves continuously
- [ ] Arrow keys control direction
- [ ] Snake cannot reverse into itself
- [ ] Food appears randomly
- [ ] Eating food grows snake and increases score
- [ ] Collision with wall ends game
- [ ] Collision with self ends game
- [ ] Game over screen shows final score
- [ ] Restart button works
- [ ] UI is visually polished with glow effects
