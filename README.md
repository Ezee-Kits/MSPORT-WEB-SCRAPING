# MSPORT Betting Scraper

The **MSPORT Betting Scraper** is designed to collect upcoming football match data from the MSPORT website. The scraper fetches match details, including odds for home win, draw, and away win, and saves the data into a CSV file for further analysis or use in betting strategies.

## 📌 Features

- **Automated Data Scraping**: Automatically scrapes football match information and odds from the MSPORT website.
- **Scroll Automation**: Handles infinite scrolling on the MSPORT page to load additional match data.
- **CSV Output**: Outputs all relevant match details (e.g., time, teams, odds) into a CSV file for easy access and analysis.
- **Duplicate Removal**: Ensures there are no duplicate entries in the CSV file.

## 🚀 How It Works

1. **Initialization**: The script initializes a headless browser session using Selenium and navigates to the MSPORT football matches page.
2. **Page Interaction**: The script scrolls down the page multiple times to load additional matches.
3. **Data Extraction**: The match details (time, teams, odds) are scraped from the page and structured into a usable format.
4. **Data Storage**: The scraped data is saved to a CSV file.
5. **Duplicate Handling**: The script ensures that duplicate match entries are removed from the CSV file.

### Key Components:

- **Selenium**: Used for browser automation, including scrolling and interacting with web elements.
- **Data Structuring**: Organizes the match information into dictionaries for structured data storage.
- **CSV File Management**: Manages saving the match data into CSV files and ensuring no duplicates.

## 🛠️ Requirements

Make sure to have the following dependencies installed:

- **Python 3.x**
- **Selenium**
- **Pandas**
- **BeautifulSoup**
- **LXML**

Install the required dependencies using pip:
```bash
pip install selenium beautifulsoup4 pandas lxml
```

## 🏃 How to Run the Script

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Ezee-Kits/MSPORT-Betting-Scraper.git
   ```

2. **Set Up ChromeDriver**:  
   Download and install [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) to match your Chrome version, and ensure it's in your system path.

3. **Run the Python Script**:
   ```bash
   python msport_scraper.py
   ```

4. **View Results**:  
   The scraped data will be saved in the specified `saving_path_csv` directory as `MSPORT.csv`.

## 📁 CSV Output

The CSV file will contain the following columns:
- **TIME**: The time of the match.
- **HOME TEAM**: The home team’s name.
- **AWAY TEAM**: The away team’s name.
- **HOME ODD**: Odds for the home team to win.
- **DRAW ODD**: Odds for a draw.
- **AWAY ODD**: Odds for the away team to win.
- **BOOKMAKER**: Always set to "MSPORT" for this scraper.

## 🔧 Future Enhancements

- **Real-Time Updates**: Add real-time updates to scrape new matches as they are added.
- **Error Handling**: Enhance error handling for unexpected website changes.
- **Multi-Sport Support**: Extend the script to scrape other sports in addition to soccer.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🤝 Contributing

Contributions are welcome! Please feel free to open issues, suggest improvements, or submit pull requests.
