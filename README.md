# doordec

Door decoration generator for dormitory rooms. Creates printable PDF name plates with memes for each room.

## Features

- Reads resident rosters from Excel files
- Groups residents by room number
- Generates A4 landscape PDF pages with:
  - Two resident names per page (diagonal layout)
  - Random cat/dog memes as center artwork
  - Clean, modern design with rounded name plates

## Usage

1. Place roster Excel file in `data/`
2. Add meme images to `data/cat_memes/` or `data/dog_memes/`
3. Edit config in `scripts/main.ipynb`:
   ```python
   ROSTER_PATH = '../data/your_roster.xlsx'
   MEMES_PATH = '../data/cat_memes/'
   OUTPUT_PATH = '../out/output.pdf'
   BED_SPACE_PREFIX = 'F-3103'  # Filter by building/floor
   ```
4. Run the notebook
5. Find output PDF in `out/`

## Requirements

- pandas
- matplotlib
- Pillow
- openpyxl (for Excel files)
- tqdm

Optional (for Reddit meme download):
- praw
- requests

## License

MIT
