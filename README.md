🚀 Особенности
Высокая производительность - до 500 товаров в час

Обход защиты - ротация User-Agent, случайные задержки

Гибкая фильтрация - поиск по характеристикам товаров

Устойчивость к ошибкам - автоматические повторы запросов

⚙️ Установка
Клонируйте репозиторий:

bash
git clone https://github.com/Beks-7/Parsing_Kaspi.git
cd Parsing_Kaspi
Установите зависимости:

bash
pip install -r requirements.txt
Скачайте ChromeDriver и поместите в папку проекта

🛠 Использование
Базовый запуск:
bash
python kaspi_parser.py
Конфигурация:
python
# Основные настройки
BASE_URL = "https://kaspi.kz/shop/c/notebooks/"  # Категория для парсинга
OUTPUT_FILE = "kaspi_notebooks.csv"              # Выходной файл
MAX_RETRIES = 3                                  # Попытки переподключения
DELAY_RANGE = (1, 3)                             # Случайные задержки (сек)

# Настройки браузера
HEADLESS_MODE = True                             # Фоновый режим
USER_AGENT_ROTATION = True                       # Ротация User-Agent
Фильтрация товаров:
python
# Измените условие для своей задачи
if max_memory and max_memory.replace('.', '').isdigit() and float(max_memory) >= 32:
📊 Выходные данные
Скрипт создает CSV-файл со следующей структурой:

csv
name,price,link,max_memory,specs
Ноутбук Apple MacBook Air 13,799990,https://kaspi.kz/shop/p/...,64,"{'Модель': 'MacBook Air', 'Память': '64 ГБ'}"

Ноутбук ASUS ROG Strix,599990,https://kaspi.kz/shop/p/...,32,"{'Модель': 'ROG Strix', 'Память': '32 ГБ'}"
⚠️ Важные замечания
Соблюдайте правила сайта Kaspi.kz

Для коммерческого использования:

Добавьте прокси-серверы

Используйте сервисы решения капчи

Увеличьте задержки между запросами

Не уменьшайте DELAY_RANGE ниже 1 секунды

📚 Зависимости
Python 3.7+

Selenium

BeautifulSoup4

📂 Структура проекта
text
Parsing_Kaspi/
├── kaspi_parser.py     # Основной скрипт
├── requirements.txt    # Зависимости
├── output/             # Папка с результатами
│   └── kaspi_notebooks.csv
└── README.md           # Документация
