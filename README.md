# Kaspi Shop Parser

This script is designed to parse information about laptops from the Kaspi Shop website.

## Installation

1. Install the required dependencies by running:

    ```bash
    pip install selenium beautifulsoup4
    ```

2. Download [ChromeDriver](https://sites.google.com/chromium.org/driver/) and specify the path to it in the `driver_path` variable in the code.

## Usage

1. Run the script:

    ```bash
    python kaspi_parser.py
    ```

2. Enter the URL of the Kaspi Shop page with laptops in the `url` variable.

3. Wait for the parsing process to complete.

4. The results will be saved in the `output.txt` file.

## Dependencies

- Python 3.x
- Selenium
- BeautifulSoup4


---
**Note:** Make sure you have downloaded and installed ChromeDriver, and specified the correct path in the code.
