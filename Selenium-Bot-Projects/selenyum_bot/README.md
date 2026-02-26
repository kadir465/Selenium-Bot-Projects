# Instagram Follower Extraction Bot

This directory contains Object-Oriented Python scripts that automate the process of logging into Instagram, navigating to a user profile, and extracting the followers list using Selenium WebDriver. 

The project demonstrates a clear progression from basic DOM interaction to handling advanced dynamic web content.

## Project Evolution & Files

### 1. Basic Extraction (`instagram_bot1.py`)
A foundational script that establishes the core automation workflow.
* **Features:** Logs into Instagram using provided credentials, navigates to the user's profile, and opens the followers dialog box. It extracts the initially visible followers using CSS selectors.

### 2. Advanced Dynamic Scrolling (`instagram_bot2.py`)
A robust, production-like script designed to handle modern, dynamic single-page applications (SPAs).
* **Features:**
  * **Pop-up Handling:** Uses `try-except` blocks and explicit waits to automatically detect and dismiss cookie consent banners and "Turn on Notifications" pop-ups.
  * **JavaScript Injection:** Executes custom JavaScript (`arguments[0].scrollTop = arguments[0].scrollHeight`) directly within the browser context to scroll down the followers dialog box.
  * **Infinite Scroll Logic:** Implements a `while` loop that continuously checks the `scrollHeight` to determine if new followers have loaded, breaking only when the bottom of the list is reached.
  * **Data Integrity:** Uses a Python `set()` to ensure the final list contains completely unique usernames, preventing duplicates caused by dynamic DOM rendering.

## Technologies and Concepts Demonstrated

* **Python 3.x**
* **Selenium WebDriver:** Chrome options configuration (e.g., `--disable-notifications`).
* **Advanced Explicit Waits:** Utilizing `WebDriverWait` and `expected_conditions` (EC) for highly reliable element targeting (e.g., `element_to_be_clickable`, `presence_of_element_located`).
* **JavaScript DOM Manipulation:** Bypassing standard Selenium limitations to scroll inner container elements.
* **Error Handling:** Graceful failure and resource cleanup using `try-except-finally` blocks and `driver.quit()`.

## Setup and Usage

1. **Install Dependencies:**
   Ensure you have the required libraries installed:
   ```bash
   pip install selenium chromedriver-autoinstaller

2. Credential Configuration (CRITICAL):
The scripts import credentials from an external file to prevent exposing sensitive data in version control. Create a file named instagram_info.py in this directory and add your test credentials:
# instagram_info.py
username = "your_test_account_username"
password = "your_test_account_password"

3. Run the Script:
python instagram_bot2.py