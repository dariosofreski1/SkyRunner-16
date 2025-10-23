# SkyRunner-16 (16-bit Assembly Plane Game)

A small video game written in **16-bit assembly** for a **custom CPU simulator (4 registers)**.
Features sprite tiles, keyboard interrupt handling, scrolling background, score, and a start screen.

## Features
- Keyboard **ISR** (interrupt service routine) for input
- **VSync**/frame wait for steady refresh
- **Sprite tiles** (plane, clouds, obstacles)
- **Scrolling view** & start screen
- Score/sum tracking and simple rules (no revisits)

## How to Run
1. Open the custom **16-bit simulator** used in course *Systems 1*.
2. Load `game.asm` (or assembled binary if your simulator requires it).
3. Set entry point to `main` (or program start) and run.

> If your simulator supports memory-mapped I/O, the game writes to display ports `8/9` and handles input on port `6` (adjust if your version differs).

## Controls
- `A / D` – move plane left/right  
- `S` – start/take off  
(Adapt if your keys differ.)

## Code Map
- `isr` – keyboard interrupt & vsync flag  
- `load_vram_tiles` – upload tile definitions  
- `draw_plane`, `draw_cloud` – sprite drawing  
- `scroll_screen` – camera/viewport movement  
- `move_plane` – input → position update  
- `game_loop` – main loop (draw → scroll → wait)

## Screenshots
See **/docs** for screenshots/GIF.

## Notes
Written for the **FAMNIT Systems 1** course on a custom 16-bit simulator with 4 registers.

