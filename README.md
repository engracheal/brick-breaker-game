# brick-breaker-game
Brick Breaker is a web-based arcade game where players control a paddle to bounce a ball and destroy bricks to defend their kingdom from invading magical orbs. The game features multiple levels, various power-ups, and an engaging scoring system.


# 🎮 Brick Breaker Game - Defend the Kingdom

(image.png)

A modern take on the classic brick breaker game with enhanced features including power-ups, particle effects, sound effects, and progressive difficulty system.

## 🌟 Overview

**Brick Breaker** is a web-based arcade game where players control a paddle to bounce a ball and destroy bricks to defend their kingdom from invading magical orbs. The game features multiple levels, various power-ups, and an engaging scoring system.

### 🎯 Game Narrative
*The kingdom's defensive walls (bricks) are under siege from magical invading orbs. As the royal defender, you must use your enchanted paddle to redirect these orbs back at the walls, protecting the kingdom while earning glory and high scores!*

---

## ✨ Features

### Core Gameplay
- ⚔️ **Smooth paddle controls** with keyboard input (Arrow Keys / A,D)
- 🎯 **Precise ball physics** with angle-based bouncing
- 🧱 **Multi-hit bricks** that require multiple strikes to destroy
- 💥 **Particle effects** when bricks break
- 🔊 **Dynamic sound effects** for all game events

### Power-Up System
- 🟢 **Wide Paddle** - Extends paddle width for 10 seconds
- 🔴 **Extra Life** - Grants an additional life
- 🟡 **Slow Ball** - Reduces ball speed for 8 seconds
- 🔵 **Multi-Ball** - Spawns additional balls

### Progression & Difficulty
- 📈 **Progressive difficulty** - Ball speed increases with each level
- 🎚️ **Dynamic brick patterns** across different levels
- 🏆 **High score tracking** with persistent storage
- ⭐ **5-tier scoring system** based on brick colors

### User Interface
- 🎨 **Modern gradient design** with glowing effects
- 📊 **Real-time HUD** displaying Lives, Score, Level, and Remaining Bricks
- ⏸️ **Pause functionality** (Press P or ESC)
- 📖 **Comprehensive instructions menu**
- 🏠 **Polished start/game over screens**

---

## 🚀 How to Play

### Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/engracheal/brick-breaker-game/tree/main
cd brick-breaker-game
```

2. **Open the game:**
   - Simply open `index.html` in any modern web browser
   - No installation or dependencies required!

3. **Play online:**
   - Visit: https://github.com/engracheal/brick-breaker-game/tree/main

### Controls

| Key | Action |
|-----|--------|
| `←` `→` or `A` `D` | Move paddle left/right |
| `SPACE` or `ENTER` | Launch ball |
| `P` or `ESC` | Pause/Resume game |
| `🔊` Button | Toggle sound on/off |

### Game Rules

1. **Objective:** Destroy all bricks to advance to the next level
2. **Lives:** You start with 3 lives. Lose a life when the ball falls below the paddle
3. **Winning:** Clear all bricks across all levels
4. **Losing:** Run out of lives before clearing all bricks

### Scoring System

| Brick Color | Points | Position |
|-------------|--------|----------|
| 🔴 Red | 10 points | Top row |
| 🟠 Orange | 8 points | Second row |
| 🟡 Yellow | 6 points | Middle row |
| 🟢 Green | 4 points | Fourth row |
| 🔵 Blue | 2 points | Bottom row |

---

## 🏗️ Technical Architecture

### Technology Stack
- **HTML5 Canvas** - For rendering game graphics
- **Vanilla JavaScript** - Game logic and mechanics
- **Web Audio API** - Dynamic sound generation
- **CSS3** - Modern UI styling with animations


### Class Architecture

The game follows **Object-Oriented Programming** principles:

#### Core Classes

**`Game`** - Main game controller
- Manages game state (menu, playing, paused, gameover)
- Handles game loop and rendering
- Coordinates all game objects

**`Paddle`** - Player-controlled paddle
- Movement logic with boundary detection
- Power-up effects (width extension)
- Collision detection with ball

**`Ball`** - Game ball with physics
- Movement with velocity vectors
- Collision detection (walls, paddle, bricks)
- Speed progression system

**`Brick`** - Destructible obstacles
- Multi-hit capability
- Color-based scoring
- Visibility state management

**`PowerUp`** - Collectible bonuses
- 4 different types with unique effects
- Falling animation
- Collision detection with paddle

**`Particle`** - Visual effects system
- Explosion effects when bricks break
- Physics-based movement
- Life cycle management

**`SoundManager`** - Audio system
- Web Audio API integration
- Event-based sound triggers
- Mute/unmute functionality

---

## 🎮 Game Mechanics

### Collision Detection

**Ball-Paddle Collision:**
```javascript
- Detects ball contact with paddle surface
- Calculates bounce angle based on hit position
- Applies velocity changes for realistic physics
```

**Ball-Brick Collision:**
```javascript
- Uses AABB (Axis-Aligned Bounding Box) detection
- Reverses ball direction on contact
- Handles multi-hit brick degradation
```

**Power-up Collection:**
```javascript
- Checks overlap between falling power-ups and paddle
- Triggers power-up effect on collection
- Removes collected power-ups from game
```

### Difficulty Progression

| Level | Ball Speed | Multi-Hit Bricks | Power-up Chance |
|-------|-----------|------------------|-----------------|
| 1 | 4.0 | 0% | 20% |
| 2 | 4.3 | 0% | 20% |
| 3+ | 4.6+ | 30% | 20% |

### Risk Management

**Player must navigate:**
- ⚡ Increasing ball speed as levels progress
- 🧱 Bricks requiring multiple hits (Level 3+)
- ⏰ Limited reaction time at higher speeds
- 💀 Limited lives (3) to complete all levels

**Balancing mechanisms:**
- 🎁 Power-ups provide strategic advantages
- 🎯 Paddle angle affects ball direction for control
- 📊 Progressive difficulty curve maintains engagement

---

## 📸 Screenshots

### Main Menu
[Main Menu](image-1.png)
*Clean and intuitive start screen with game title and options*

### Gameplay
[Active Gameplay](image-2.png)
*Dynamic gameplay with HUD, paddle, ball, and colorful bricks*

### Power-ups
[Power-up Collection] (image-3.png)
*Visual feedback when collecting power-ups*

### Game Over
[Game Over Screen](image-4.png)
*Final score display with restart options*

---

## 🧪 Testing & Quality Assurance

### Tested Scenarios

✅ **Mechanics Testing:**
- Paddle movement and boundary detection
- Ball physics and collision accuracy
- Brick destruction and scoring
- Power-up spawning and effects

✅ **UI/UX Testing:**
- Menu navigation flow
- HUD updates in real-time
- Pause/resume functionality
- Game state transitions

✅ **Performance Testing:**
- Smooth 60 FPS rendering
- Particle system optimization
- Memory leak prevention
- Browser compatibility

✅ **Edge Cases:**
- Multiple balls on screen
- Rapid brick destruction
- Power-up stacking
- Level transitions

### Browser Compatibility

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Fully Supported |
| Firefox | 88+ | ✅ Fully Supported |
| Safari | 14+ | ✅ Fully Supported |
| Edge | 90+ | ✅ Fully Supported |

---

## 🚧 Known Limitations & Future Enhancements

### Current Limitations
- Single-player only (no multiplayer mode)
- Fixed brick patterns (no level editor)
- Web Audio API requires user interaction to enable

### Planned Features
- 🎨 **Level Editor** - Create custom brick patterns
- 🏅 **Leaderboard System** - Global high score tracking
- 🎵 **Background Music** - Ambient soundtrack
- 📱 **Mobile Support** - Touch controls for mobile devices
- 🌍 **More Levels** - Extended campaign with boss levels
- 🎁 **More Power-ups** - Shield, fireball, explosive ball
- 💾 **Save System** - Resume progress across sessions

---

## 👥 Developer 
- **[Ampumuza Recheal]** - Lead Developer & Game Designer

## 📚 Resources & Documentation

### Project Links
- 
- 🎥 [Video Demo] 
- 🌐 [Play Online] https://github.com/engracheal/brick-breaker-game/tree/main
- 💻 [Source Code] (https://github.com/engracheal/brick-breaker-game/tree/main)

### Development Resources
- [HTML5 Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
- [Game Development Patterns](https://gameprogrammingpatterns.com/)

---

## 📝 License

This project was created as coursework for educational purposes.

**Academic Use Only** - Not licensed for commercial distribution.

---

## 🙏 Acknowledgments

- **Instructor:** Mr. Bazigu Alex
- **Moderator:** Dr. David Kakeeto
- **Inspiration:** Classic Atari Breakout (1976)
- **University:** Faculty of Science and Technology

---

## 📞 Contact & Support

For questions or feedback about this project:

- **GitHub Issues:** [Create an issue](https://github.com/engracheal/brick-breaker-game/issues)
- **Email:** (ampumuzarecheal152@gmail.com)

---

## 🎉 Enjoy the Game!

*Defend the kingdom, break those bricks, and set a new high score!*

### Quick Start Commands

```bash
# Clone the repository
git clone https://github.com/engracheal/brick-breaker-game/tree/main

# Navigate to directory
cd brick-breaker-game

# Open in browser (Mac)
open index.html

# Open in browser (Windows)
start index.html

# Open in browser (Linux)
xdg-open index.html
```
