# Vin and Michelle Wedding Game

A pygame-based side-scrolling shooter game built with pygbag for web deployment.

## Live Demo

[Play the game here!](https://yourusername.github.io/pichMed-pygame/)

## Game Features

- Multiple themed levels with different enemies and backgrounds
- Progressive difficulty with increasing speed
- Sound effects and background music
- High score tracking
- Responsive controls (keyboard and mouse)

## Controls

- **Arrow Keys**: Move ship up/down
- **Spacebar**: Fire bullets
- **P**: Pause/Resume game (only when game is active and no intro popup is visible)
- **E**: Enter/Continue (only when Enter button is visible on screen)
- **R**: Restart (only when Restart button is visible on screen)
- **Q**: Quit (hard exit - may leave game in stuck state, use with caution)

## Development

### Prerequisites

- Python 3.9+
- pygame
- pygbag

### Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/pichMed-pygame.git
cd pichMed-pygame
```

2. Create and activate virtual environment:
```bash
python -m venv pichMed_env
source pichMed_env/bin/activate  # On Windows: pichMed_env\Scripts\activate
```

3. Install dependencies:
```bash
pip install pygame pygbag
```

### Running Locally

1. For desktop version:
```bash
cd source
python main.py
```

2. For web version:
```bash
cd source
python -m pygbag main.py
```

## Deployment to GitHub Pages

### Automatic Deployment (Recommended)

The repository is set up with GitHub Actions for automatic deployment:

1. Push your changes to the `main` branch
2. The workflow will automatically build and deploy to GitHub Pages
3. Your game will be available at `https://yourusername.github.io/pichMed-pygame/`

### Manual Deployment

If you prefer manual deployment:

1. Run the build script:
```bash
python build_for_github_pages.py
```

2. Commit and push the `docs` folder:
```bash
git add docs/
git commit -m "Update game build"
git push origin main
```

3. Configure GitHub Pages:
   - Go to repository Settings
   - Navigate to Pages section
   - Set source to "Deploy from a branch"
   - Select "main" branch and "/docs" folder
   - Save settings

## Game Assets

The game includes multiple themes:
- Surfer zombies
- Mariachi zombies
- Baseball player zombies
- Cupid zombies
- Ant zombies
- Grandma zombies
- Abandoned Bride zombies

Each theme has custom sprites, backgrounds, and music.

## Project Structure

```
pichMed-pygame/
├── source/                 # Main game source code
│   ├── main.py            # Game entry point
│   ├── settings.py        # Game configuration
│   ├── themes/            # Game themes and assets
│   ├── sounds/            # Audio files
│   ├── fonts/             # Custom fonts
│   └── build/             # Build output
├── docs/                  # GitHub Pages deployment files
├── .github/workflows/     # GitHub Actions
└── build_for_github_pages.py  # Build script
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test the game
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Credits

Created for Vin and Michelle's wedding celebration!
