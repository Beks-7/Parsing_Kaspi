Kaspi Shop Parser
This Python script parses product data from Kaspi.kz marketplace with anti-bot protection bypass and dynamic content handling.

Features
High performance: Parses 500+ products per hour

Bot protection bypass: User-Agent rotation, random delays, headless browsing

Fault tolerance: Request retries and exception handling

Structured data: Automatic CSV conversion

Flexible filtering: Product filtering by specifications (e.g., laptops with 32+ GB RAM)

Installation
Clone the repository:


git clone https://github.com/yourusername/kaspi-parser.git
cd kaspi-parser
Install dependencies:


pip install -r requirements.txt
Install ChromeDriver:

Download the latest version from official site

Specify the driver path in the script (line 22 in kaspi_parser.py)

Usage
Basic execution:

python kaspi_parser.py
Configuration parameters (modify in code):
python
# Main settings
BASE_URL = "https://kaspi.kz/shop/c/notebooks/"  # Category to parse
OUTPUT_FILE = "kaspi_notebooks.csv"              # Output filename
MAX_RETRIES = 3                                  # Connection retries
DELAY_RANGE = (1, 3)                             # Random delays (seconds)

# Browser settings
HEADLESS_MODE = True                             # Background mode
USER_AGENT_ROTATION = True                       # User-Agent rotation
Advanced options:
Specification filtering
Modify the condition in code:

python
if max_memory and max_memory.isdigit() and int(max_memory) >= 32:
Parse other categories
Change BASE_URL to desired category:

python
BASE_URL = "https://kaspi.kz/shop/c/smartphones/"
Add proxy support
Uncomment in code:

python
# options.add_argument("--proxy-server=ip:port")
Output Data
CSV file structure example:

csv
name,price,link,max_memory,specs
Apple MacBook Air 13,799990,https://kaspi.kz/shop/p/...,64,"{'Model': 'MacBook Air', 'Memory': '64 GB'}"
ASUS ROG Strix,599990,https://kaspi.kz/shop/p/...,32,"{'Model': 'ROG Strix', 'Memory': '32 GB'}"
Important Notes
Respect robots.txt
Check parsing permissions for each domain.

Use delays
Don't reduce DELAY_RANGE values to avoid blocking.

For commercial use:

Implement proxy rotation

Add CAPTCHA solving

Use distributed architecture

Dependencies
Python 3.x

Selenium

BeautifulSoup4

