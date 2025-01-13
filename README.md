# 📊 Product Price Tracker & Telegram Bot

## 📖 Overview
This project consists of a **Product Price Tracker** and a **Telegram Bot** that allows users to:
- Analyze historical product prices from the **Hong Kong Price Watch API**.
- Perform price predictions using time series forecasting (ARIMA model).
- Interact with a Telegram Bot to query product prices, view price trends, and receive purchase recommendations.

---

## 🛠️ Features
1. **Historical Price Data Retrieval**:
   - Uses the **Hong Kong Price Watch API** to fetch historical product prices.
   - Cleans and consolidates data into a structured format for analysis.

2. **Price Prediction**:
   - Utilizes the **ARIMA model** to forecast future product prices based on historical trends.
   - Provides actionable recommendations to users: whether to buy now or wait.

3. **Telegram Bot Integration**:
   - A bot built with the **pyTelegramBotAPI** to make data queries more accessible.
   - Features:
     - **Product Search**: Users can search for a product and receive a price trend graph.
     - **Price Forecasting**: Predicts price movements and advises users.
     - **Data Update**: Keeps the product database up-to-date.
     - **Session Management**: Allows users to start and terminate bot sessions.

---

## 📂 Project Structure
```
├── consolidated_function.py    # Core functions for data retrieval and processing
├── tgBot.py                     # Telegram bot implementation
├── database2.csv                # Sample product database (for bot usage)
├── sample_plot.png              # Sample price trend plot
└── output.mp4                   # Goodbye video for bot termination
```

---

## 📋 Requirements
- Python 3.8+
- Libraries:
  - pandas
  - fuzzywuzzy
  - requests
  - statsmodels
  - matplotlib
  - pyTelegramBotAPI
  - tqdm

Install the required libraries using:
```bash
pip install -r requirements.txt
```

---

## 🔧 Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/product-price-tracker-bot.git
   cd product-price-tracker-bot
   ```

2. Create a **database file** (`database2.csv`) with the necessary product information.

3. Update your **Telegram Bot Token** in `tgBot.py`:
   ```python
   BOT_TOKEN = "Your token"
   ```

4. Run the bot:
   ```bash
   python tgBot.py
   ```

---

## 📈 How It Works
1. **Historical Price Analysis**:
   - The `consolidated_function.py` script retrieves historical price data from the API.
   - The data is cleaned, structured, and prepared for analysis.

2. **Price Forecasting**:
   - The `forecast_price` function uses the ARIMA model to predict product prices.
   - A graph showing price trends is generated using `matplotlib`.

3. **Telegram Bot**:
   - Users interact with the bot by sending messages and selecting options.
   - The bot responds with product recommendations and trend graphs.

---

## 🧩 Key Functions
- **call_price_watch_list_api**: Fetches available timestamps for historical price data.
- **price_watch_api**: Retrieves product data for a specific timestamp.
- **executing_price_watch_api**: Consolidates data retrieval and cleaning processes.
- **find_top_matches**: Finds the best-matching product names based on user input.
- **forecast_price**: Uses ARIMA to predict future product prices.
- **graph**: Plots the price trend for a given product.

---

## 📱 Bot Commands
| Command     | Description                                |
|-------------|--------------------------------------------|
| `/start`    | Start the bot interaction.                 |
| `/about`    | Learn more about the bot's features.       |
| `/update`   | Update the product database.               |
| `/end`      | Terminate the bot session.                 |

---

## 🔮 Future Enhancements
- Add more advanced machine learning models for price forecasting.
- Improve bot interactivity with more options and responses.
- Integrate additional APIs for more comprehensive product data.

---

## 📧 Contact
For any inquiries or issues, feel free to reach out via [GitHub Issues](https://github.com/your-username/product-price-tracker-bot/issues).

