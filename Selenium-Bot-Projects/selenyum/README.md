# Selenium Web Automation Basics

This directory contains introductory scripts demonstrating web browser automation, DOM interaction, and data extraction using Python and Selenium WebDriver. These mini-projects range from basic browser navigation to automated e-commerce shopping workflows.

## Files and Functionality

### 1. Basic Navigation (`selenyum_1.py`)
Demonstrates fundamental browser control.
* **Features:** Opens specific URLs, maximizes windows, navigates back and forward in history, refreshes pages, opens new tabs using JavaScript execution, switches between active windows, and properly closes browser instances.

### 2. Product Search and Extraction (`selenyum_2.py`)
An automated web scraping script targeting an e-commerce site (Monster Notebook).
* **Features:** * Locates search bars using `By.NAME`.
  * Sends keystrokes (`Keys.ENTER`) to perform searches.
  * Uses `find_elements` with CSS Selectors and Class Names to extract and print a formatted list of laptop names and their corresponding prices.

### 3. Automated Shopping Workflow (`slenyum_Alıs_Veris.py`)
An Object-Oriented script that simulates a complete user journey on `saucedemo.com`.
* **Features:**
  * **OOP Design:** Encapsulates the automation logic within the `OtoShop` class.
  * **Explicit Waits:** Uses `WebDriverWait` and `expected_conditions` (EC) to wait for elements to load, ensuring stable execution.
  * **Data Processing:** Scrapes all products on the page, converts price strings to floats, and writes the entire inventory to a local `shoping_list.txt` file.
  * **Algorithmic Action:** Dynamically finds the most expensive item in the scraped list, clicks its specific "Add to Cart" button, navigates to the checkout page, and automatically fills out the shipping information form.

## Technologies and Concepts Used

* **Python 3.x**
* **Selenium WebDriver:** For controlling the Chrome browser.
* **chromedriver-autoinstaller:** To automatically manage and update the ChromeDriver executable.
* **DOM Locators:** Finding elements via ID, NAME, CLASS_NAME, and CSS_SELECTOR.
* **Wait Strategies:** Implementing `time.sleep()` (implicit-like) and `WebDriverWait` (explicit) to handle dynamic content loading.
* **File I/O:** Writing scraped web data to text files.

## Setup and Installation

1. Install the required Python packages:
   ```bash
   pip install selenium chromedriver-autoinstaller

2. Credential Setup: The slenyum_Alıs_Veris.py script imports user credentials from an external file to keep sensitive data secure. Before running the script, create a file named instagram_info.py in this directory with the following variables:

usurname0 = "standard_user"
password0 = "secret_sauce"
firstName = "YourName"
lastName = "YourLastName"
posta = "12345"

3. Run any of the scripts from the terminal:
python selenyum_1.py