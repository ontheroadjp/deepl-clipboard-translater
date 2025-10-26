# DeepL Clipboard Translater

This script translates text from the clipboard into a specified language using the DeepL API. The source language is automatically detected.

## Requirements

- Python 3
- See `requirements.txt` for dependencies.

## Installation

1.  Install the required Python libraries using pip.

    ```bash
    python3 -m pip install -r requirements.txt
    ```

2.  Create a `.env` file in the same directory as the script.

3.  Add your DeepL API key to the `.env` file:

    ```
    DEEPL_API_KEY=your_api_key
    ```

## Usage

1.  Copy some text to your clipboard.
2.  Run the script. By default, it translates to English.

    ```bash
    python3 deepl-clipboard-translater.py
    ```

To specify a different target language, use the `-o` option. Supported languages are English (EN), Japanese (JA), Chinese (ZH), and Korean (KO).

-   Translate to Japanese:
    ```bash
    python3 deepl-clipboard-translater.py -o ja
    ```

-   Translate to Chinese:
    ```bash
    python3 deepl-clipboard-translater.py -o zh
    ```

You can pipe the output to `pbcopy` (on macOS) or `xclip` (on Linux) to copy the translation to your clipboard:
```bash
python3 deepl-clipboard-translater.py | pbcopy
```

Or redirect it to a file:
```bash
python3 deepl-clipboard-translater.py > translation.txt
```
