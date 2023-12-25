# Terminal Text Format

## About
`terminal_text_format.py` is a Python script designed to format paragraph-style text from terminal outputs. It's particularly effective with text from language models like GPT, suitable for story writing or similar tasks.

## Features
- Converts line breaks in the terminal output to spaces.
- Transforms every two spaces into double newlines (`\n\n`), aiding in text readability.

## Usage
1. **Run**: Execute the script in a terminal with `python3 terminal_text_format.py`.
2. **Input Text**: Paste or type your text into the terminal.
3. **Complete Input**: Terminate input with Enter or Ctrl+C.
4. **Output**: The script generates `output.txt` in the current directory containing the formatted text.

## Note
- Best for paragraph text (e.g., GPT outputs). May not work as intended with other text formats due to specific regex operations.
