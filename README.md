# Apartment Data Parser

## Overview
This Python project parses and cleans apartment listing data from XML files. Originally a legacy project, it extracts attributes like location and performs data cleaning tasks such as coordinate correction and fuzzy matching of area names.

## Features
- Parses apartment data from XML sources
- Cleans and standardizes coordinates and area names
- Modular design for easy extension

## Installation
1. Clone the repository: `git clone https://github.com/ahmadalsharef994/apartments-parser-legacy.git`
2. Install dependencies: `pip install -r requirements.txt`

## Usage
1. Place raw XML data in the `data/` directory.
2. Run the parser: `python parse_apartments.py`
3. Find cleaned outputs in the `output/` directory.

## Project Structure
- `parsers/`: XML parsing scripts
- `actions/`: Data cleaning utilities
- `data/`: Input data directory
- `output/`: Processed data directory

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
