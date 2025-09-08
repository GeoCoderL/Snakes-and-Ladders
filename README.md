## Snakes and Ladders (Browser Game)

A simple, single-page Snakes and Ladders game playable in your browser. Open `index.html` and play with animated dice, a classic board, and two player avatars.

### Features
- **Two-player gameplay**: Alternating turns with a single dice roll per turn
- **Animated dice**: Visual dice faces (`imgs/dice1.png` … `imgs/dice6.png`)
- **Classic board**: Background board (`imgs/board.JPG`) with ladders and snakes defined in code
- **Avatars and flags**: Visual markers for player positions and finish
- **No build required**: Pure HTML/CSS/JS; open and play

### Quick Start
1. Download or clone this repository.
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox).

If your browser blocks local file access for images/scripts, serve the folder locally:

```bash
# Option A: Python (3.x)
python -m http.server 8080
# then visit: http://localhost:8080/

# Option B: Node (http-server)
npm i -g http-server
http-server . -p 8080
# then visit: http://localhost:8080/
```

### How to Play
- Click the roll control (or the dice) to roll.
- Your token moves forward by the dice value.
- Landing on the base of a ladder climbs up; landing on a snake head slides down.
- First player to reach the final square wins.

### Controls and UI
- The main controls and game loop are implemented in `js/main.js`.
- Visual assets are located in `imgs/` and `fonts/`.
- Styles are in `css/` and `scss/`. The page currently uses prebuilt CSS.

### Tech Stack
- **HTML5**: Markup (`index.html`)
- **CSS3**: Base/reset styles in `css/`, optional Bourbon mixins in `bourbon/`
- **JavaScript (ES5/ES6)**: Game logic in `js/main.js`
- **Modernizr**: Feature detection (`js/modernizr.js`)

### Project Structure
```
bourbon/                 # SCSS mixins (no build step required for play)
css/                     # Prebuilt styles (reset and animations)
fonts/                   # Custom font(s)
imgs/                    # Board, dice faces, avatars, and UI images
js/                      # Game logic and Modernizr
scss/                    # Source styles (current build already included)
index.html               # Entry point
```

### Development Notes
- The game currently runs without a build step. If you choose to work from SCSS, integrate a Sass toolchain (e.g., Dart Sass) and point `index.html` to the compiled CSS.
- Image paths are relative to the project root; when serving locally, keep directory structure intact.

### Roadmap Ideas
- Add single-player mode vs. basic AI
- Add mobile touch improvements and responsiveness tweaks
- Add sound effects and win/lose animations
- Persist last game state in `localStorage`
- Add settings for number of players and board size

### Screenshot
If supported by your viewer, here is the board asset used by the game:

`imgs/board.JPG`

### License
This project is provided as-is for educational and personal use. If you need a specific open-source license, add one (e.g., MIT) and update this section.

### Credits
- Board, dice, and avatar images are included in `imgs/`.
- `animate.css` and `reset.css` included under `css/`.
- Bourbon mixins included under `bourbon/`.


