# Tango Puzzle Game

A constraint-based puzzle game built with Pygame where players fill a grid with sun and moon symbols following specific rules.

## Overview

Tango is a logic puzzle game where players must place sun and moon symbols on a 6x6 grid while following constraints:
- No three identical symbols in a row (horizontal or vertical)
- Equal counts of suns and moons per row/column (max 3 each)
- Constraint markers (= or x) between adjacent cells

## Key Features

- Interactive Pygame-based GUI
- Undo functionality
- Clear grid option
- Timer tracking
- Win condition detection
- Visual error highlighting

## Tech Stack

- **Pygame** - Game development and graphics
- **NumPy** - Grid state management
- **Python** - Core logic

## How to Run

1. Install dependencies:
```bash
pip install pygame numpy
```

2. Update the image path in `src/tango.py`:
```python
ASSET_PATH = "images/"
```

3. Run the game:
```bash
python src/tango.py
```

## Game Rules

- Click cells to cycle through: empty → sun → moon
- Red borders indicate constraint violations
- Locked cells (pre-filled) cannot be changed
- Constraint symbols:
  - `=` means adjacent cells must be different
  - `x` means adjacent cells must be the same

## Project Structure

```
Tango-Puzzle-Game/
├── src/
│   └── tango.py          # Main game implementation
├── notebooks/
│   └── ml_analysis.ipynb  # ML analysis for difficulty prediction
├── images/                # Game assets (sun, moon, undo, clear icons)
└── README.md
```

## ML Component

The `ml_analysis.ipynb` notebook contains machine learning analysis:
- Predicts game difficulty based on number of parameters
- Uses K-Means clustering and KNN classification
- Classifies games as Easy, Medium, or Hard

## Notes

- Requires Pygame for graphics rendering
- Image assets must be in the `images/` directory
- Game state is managed using NumPy arrays
