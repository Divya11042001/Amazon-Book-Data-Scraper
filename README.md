# 📚 Amazon Book Data Scraper

A Python-based web scraping project that extracts book data from Amazon search results and exports it to a structured Excel file.

---

## 🔍 What This Script Does

This scraper parses a locally saved Amazon search results page (`Amazon_Book01.html`) and extracts the following details for each book listing:

| Field   | Description                        |
|---------|------------------------------------|
| Name    | Title of the book                  |
| Price   | Listed price (whole number portion)|
| Reviews | Number of customer reviews         |
| Ratings | Average star rating                |
| Author  | Author name                        |
| Images  | Product image URL                  |

The extracted data is saved to an Excel file (`Bookdata01.xlsx`) using `pandas` and `openpyxl`.

---

## 🛠️ Tech Stack

- **Python 3.x**
- **BeautifulSoup4** — HTML parsing
- **pandas** — Data manipulation and Excel export
- **openpyxl** — Excel file writing backend

---

## 📁 Project Structure

```
web-scraping/
│
├── Amazon_Book01.html       # Saved Amazon search results page (input)
├── scraper.py           # Main scraping script
├── Bookdata01.xlsx      # Output Excel file with extracted book data
└── README.md
```

---

## ⚙️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Divya11042001/Amazon-Book-Data-Scraper.git
cd Amazon-Book-Data-Scraper
```

### 2. Install dependencies

```bash
pip install beautifulsoup4 pandas openpyxl
```

### 3. Add the input file

Place your saved Amazon HTML page in the project directory and name it `Amazon_Book01.html`.  
*(To get this file: open an Amazon book search in your browser → Save Page As → Webpage, Complete)*

### 4. Run the scraper

```bash
python scraper.py
```

### 5. Check the output

Open `Bookdata01.xlsx` to see all extracted book data.

---

## 📌 Notes

- This script scrapes from a **locally saved HTML file**, not by sending live requests to Amazon. This avoids IP blocking and rate limiting issues.
- Amazon's HTML structure may change over time. If the scraper stops extracting data correctly, inspect the page source and update the CSS class names accordingly.
- This script is intended for **educational purposes only**. Always review Amazon's [Terms of Service](https://www.amazon.com/gp/help/customer/display.html?nodeId=508088) before scraping.

---

## 📊 Sample Output

| Name                        | Price | Reviews | Ratings       | Author         | Images |
|-----------------------------|-------|---------|---------------|----------------|--------|
| Atomic Habits               | 599   | 12,345  | 4.8 out of 5  | James Clear    | url... |
| The Alchemist               | 299   | 8,901   | 4.7 out of 5  | Paulo Coelho   | url... |

---

## 🙋‍♀️ Author

Made by **Divya Gaikwad**  
Feel free to fork, star ⭐, and raise issues!
