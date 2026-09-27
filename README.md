# Surah Cards Generator for Anki

Generate Anki flashcards for Quran Surahs using the [Al-Quran Cloud API](https://alquran.cloud/api). Creates clean, minimal cards with Arabic (Uthmani), transliteration, and translation.

## Preview

<p align="center">
  <img src="screenshots/card-front.png" alt="Front of Anki card" width="45%">
  <img src="screenshots/card-back.png" alt="Back of Anki card" width="45%">
</p>

## Features

- **Dynamic Cards**: Pulls Surah data (Arabic, transliteration, translation) via API.
- **Customizable Range**: Generate any Surahs (e.g., `1`, `110-114`, `1,78,112`).
- **Minimal Design**: Large Arabic text (RTL), left-aligned transliteration/translation, title-case Surah names.
- **Anki-Compatible**: Outputs CSV with fields for `RomanizedTitle`, `ChapterInfo`, `Arabic`, `Transliteration`, `Translation`.

## Prerequisites

- **Python 3.8+**: Install from [python.org](https://www.python.org/downloads/).
- **Requests library**: `pip install requests`.
- **Anki**: Install from [apps.ankiweb.net](https://apps.ankiweb.net).
- An Arabic font may be required — "Traditional Arabic" or "Scheherazade" is recommended.

## Installation

1. Clone this repo:
   ```bash
   git clone https://github.com/rayyanarchy/surah-cards-anki.git
   cd surah-cards-anki
   ```

2. Install the dependency:
   ```bash
   pip install requests
   ```

3. Import the Anki note type:
   - In Anki: `File > Import` > select `surah_cards.apkg`.
   - This creates the "Surah Card" note type with templates.

## How To Use

1. Run the script to generate cards:
   ```bash
   python3 generate_surah_cards.py "110-114"
   ```
   This outputs `surahs.csv`.

2. Import into Anki:
   - `File > Import` > select `surahs.csv`.
   - Set encoding to UTF-8, and map fields to `RomanizedTitle`, `ChapterInfo`, `Arabic`, `Transliteration`, `Translation`.
   - Choose your deck (e.g., "Quran Surahs").
   - Check "Allow HTML in fields".

## License

This project is open source and available under the [MIT License](LICENSE).
