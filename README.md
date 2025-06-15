Kaspi.kz Product Parser
This Python script parses product data from Kaspi.kz marketplace with anti-bot protection bypass and dynamic content handling.

Features
⚡ High performance: Parses 500+ products per hour

🛡️ Bot protection bypass: User-Agent rotation, random delays

🔁 Fault tolerance: Automatic retries and exception handling

📊 Structured data: Output in CSV format

🔍 Flexible filtering: Filter products by specifications

Installation
Clone the repository:

bash
git clone https://github.com/yourusername/kaspi-parser.git
cd kaspi-parser
Install dependencies:

bash
pip install -r requirements.txt
Download ChromeDriver and place it in the project directory

Usage
Basic execution:
bash
python kaspi_parser.py
Configuration:
Modify these parameters in the script:

python
# Main settings
BASE_URL = "https://kaspi.kz/shop/c/notebooks/"  # Category to parse
OUTPUT_FILE = "kaspi_notebooks.csv"              # Output filename
MAX_RETRIES = 3                                  # Connection retries
DELAY_RANGE = (1, 3)                             # Random delays (seconds)

# Browser settings
HEADLESS_MODE = True                             # Headless mode
USER_AGENT_ROTATION = True                       # User-Agent rotation
Filter customization:
Change the filtering condition in the code:

python
if max_memory and max_memory.replace('.', '').isdigit() and float(max_memory) >= 32:
Output Example
The script generates a CSV file with the following structure:

name	price	link	max_memory	specs
Apple MacBook Air 13	799990	https://kaspi.kz/shop/p/...	64	{'Model': 'MacBook Air', ...}
ASUS ROG Strix	599990	https://kaspi.kz/shop/p/...	32	{'Model': 'ROG Strix', ...}
Important Notes
Respect Kaspi.kz's robots.txt and terms of service

Add proxy support for commercial use:

python
# Uncomment in setup_driver()
# options.add_argument("--proxy-server=ip:port")
Consider adding CAPTCHA solving services for heavy usage

Dependencies
Python 3.7+

Selenium

BeautifulSoup4
