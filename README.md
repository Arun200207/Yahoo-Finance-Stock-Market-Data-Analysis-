# 📈 Stock EDA Dashboard

A powerful yet simple web application for performing **Exploratory Data Analysis (EDA)** on stock market data using **Streamlit** and **Yahoo Finance** (via `yfinance`). This dashboard provides insightful visualizations and statistical summaries to help traders, analysts, and data enthusiasts understand stock trends over custom date ranges.

---

## 🌟 Features

- 🔎 Search and analyze any publicly traded stock using its ticker symbol (e.g., `AAPL`, `TSLA`, `GOOGL`)
- 🧾 View raw historical data pulled from Yahoo Finance
- 📊 Summary statistics for stock metrics (Open, High, Low, Close, Volume)
- 📉 Time-series chart of closing prices
- 📈 Customizable Moving Average overlay (e.g., 20-day MA)
- 📦 Volume traded visualization
- 🔥 Correlation heatmap for identifying relationships between features
- 🚀 Fast and interactive UI built with Streamlit

---

## 📸 Screenshots

> *(Replace with real screenshots once the app is running)*

### 📊 Dashboard View
![Dashboard](screenshots/dashboard.png)

### 📈 Moving Average Overlay
![Moving Average](screenshots/moving_average.png)

---

## 🛠️ Tech Stack

| Technology   | Description                       |
|--------------|-----------------------------------|
| Streamlit    | UI framework for building data apps |
| yfinance     | Python wrapper for Yahoo Finance API |
| Pandas       | Data manipulation and analysis     |
| Matplotlib   | Plotting static graphs             |
| Seaborn      | Advanced data visualization        |

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/stock-eda-dashboard.git
cd stock-eda-dashboard

## 📦 Installation

### 2. Create & Activate a Virtual Environment *(Optional but Recommended)*

To ensure a clean Python environment and avoid dependency conflicts, it’s recommended to use a virtual environment.

#### 🐧 Linux / macOS

```bash
# Create a virtual environment named 'venv'
python3 -m venv venv

# Activate the virtual environment
source venv/bin/activate


## 📦 Installation

### 3. Install Dependencies

After setting up your virtual environment, you’ll need to install the required Python libraries.

#### 🔧 Using `requirements.txt`

If your project includes a `requirements.txt` file, install all dependencies by running:

```bash
pip install -r requirements.txt


## 📦 Installation

### 4. Run the Application

Once your virtual environment is activated and all dependencies are installed, you can launch the app locally using the Streamlit CLI:

```bash
streamlit run app.py


## 🧾 How to Use the App

Once the application is running, follow these steps to explore stock data:

### 1. 🔍 Enter a Stock Ticker

- Use the **sidebar input field** to enter a valid stock ticker symbol.
- Examples:  
  - `AAPL` (Apple)  
  - `GOOGL` (Alphabet/Google)  
  - `TSLA` (Tesla)  
  - `MSFT` (Microsoft)

> ⚠️ Ticker symbols are case-insensitive but must be valid and available on Yahoo Finance.

---

### 2. 📅 Select a Date Range

- Use the **date selectors** in the sidebar to specify the time period you want to analyze.
- You can explore daily stock activity over days, months, or years.

---

### 3. 📈 Analyze the Stock Data

The dashboard displays multiple views and visualizations to help you understand trends and insights:

#### 📄 Raw Data Table
- View the historical stock data fetched from Yahoo Finance.
- Columns include: `Open`, `High`, `Low`, `Close`, `Adj Close`, and `Volume`.

#### 📊 Summary Statistics
- Displays key metrics such as:
  - Mean, standard deviation, minimum, and maximum values for each column.
  - Great for a quick statistical overview.

#### 📉 Closing Price Line Chart
- A time-series plot showing the closing price of the stock.
- Helps visualize trends over the selected date range.

#### 🔁 Moving Average Chart
- Apply a **customizable moving average (e.g., 20-day MA)** to the closing price.
- Use the slider in the sidebar to adjust the MA period.

#### 📦 Volume Traded Bar Chart
- Visualize how much stock was traded each day.
- Can help identify volume spikes during price movements.

#### 🔍 Correlation Heatmap
- Shows the correlation between all numerical variables (e.g., Volume, High, Low).
- Helps identify relationships or dependencies between stock metrics.

---

### ✅ Example Workflow

1. Enter `AAPL` in the ticker input
2. Choose `2023-01-01` to `2023-12-31` as your date range
3. Set the moving average window to `20`
4. Review the closing price chart and correlation heatmap to detect trends and relationships

---

> 💡 Pro Tip: Try analyzing different tickers across sectors (e.g., tech, pharma, energy) to gain broader market insights.


## 🌐 Deployment

You can deploy your Stock EDA app online using **Streamlit Cloud** in just a few steps.

---

### 🚀 Deploying on Streamlit Cloud

Follow the steps below to host your app for free on [Streamlit Cloud](https://streamlit.io/cloud):

#### 1. 🗂️ Push the App to GitHub

Make sure your project files are in a public or private GitHub repository. Your repo should include:



---

#### 2. 🔗 Connect to Streamlit Cloud

1. Go to: [https://streamlit.io/cloud](https://streamlit.io/cloud)
2. Sign in with your GitHub account
3. Click **"New App"**

---

#### 3. 📄 Configure App Settings

In the deployment form:

- **Repository**: Select your repo (e.g., `your-username/stock-eda-dashboard`)
- **Branch**: Choose your working branch (usually `main`)
- **Main file path**: Enter `app.py`

---

#### 4. ⚙️ Ensure `requirements.txt` is Present

Streamlit Cloud uses this file to install dependencies.  
If you don’t have one, generate it using:

```bash
pip freeze > requirements.txt


## ⚠️ Known Limitations

While this Stock EDA app provides useful insights, please be aware of the following limitations:

- **Single Ticker Analysis Only**  
  The app currently supports analyzing only one stock ticker at a time. Multi-ticker comparisons are not yet implemented.

- **Data Source Restrictions**  
  Data is fetched from Yahoo Finance via the `yfinance` library, which can sometimes experience delays or missing data for certain tickers or date ranges.

- **No Intraday or Real-Time Data**  
  The app uses daily historical stock data only. Intraday or real-time updates are not supported.

- **Limited Technical Indicators**  
  Currently, only simple moving averages (MA) are included. Advanced technical indicators like RSI, MACD, or Bollinger Bands are not part of this version.

- **No Export or Download Feature**  
  Data and charts cannot be directly exported or downloaded from the app.

- **UI and Performance**  
  Designed for simplicity; performance may degrade when analyzing very long date ranges or with slower internet connections.

---

> ⚙️ These limitations are expected to be addressed in future updates. Contributions and suggestions are welcome!

## 🔮 Planned Features

We are continuously working to improve the Stock EDA app. Here are some features planned for future releases:

- [ ] **Multi-Ticker Support**  
  Analyze and compare multiple stock tickers simultaneously.

- [ ] **Interactive Candlestick Charts**  
  Incorporate Plotly-based candlestick charts for more detailed price visualization.

- [ ] **Export Data Functionality**  
  Allow users to export filtered datasets and charts as CSV or image files.

- [ ] **Advanced Technical Indicators**  
  Add indicators such as RSI, MACD, Bollinger Bands, and others for deeper analysis.

- [ ] **Intraday and Real-Time Data**  
  Integrate intraday stock data updates for near real-time monitoring.

- [ ] **Docker Support**  
  Provide Docker configuration for easy containerized deployment.

- [ ] **User Authentication and Profiles**  
  Enable user accounts to save preferences and analyses.

- [ ] **Enhanced UI/UX Improvements**  
  Improve the interface with more customization options and responsive design.

---

> 💡 Got ideas or want to contribute? Feel free to submit issues or pull requests on GitHub!


## 🤝 Contributing

Contributions are always welcome! Whether you want to report a bug, suggest a feature, or improve the codebase, here’s how you can get involved:

### How to Contribute

1. **Fork the repository**  
   Click the **Fork** button at the top right of the GitHub repo page to create your own copy.

2. **Create a new branch**  
   It’s best to work on a feature or bugfix branch separate from `main`:
   ```bash
   git checkout -b feature/your-feature-name


## 📝 License

This project is licensed under the **MIT License** — a permissive open-source license that allows you to freely use, modify, and distribute the software.

---

### Summary of the MIT License

- Permission is granted, free of charge, to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software.
- The software is provided "as is", without warranty of any kind.
- The full license text can be found in the [LICENSE](LICENSE) file included in this repository.

---

### License File

Make sure to include a `LICENSE` file in your repository root with the following content:

```text
MIT License

Copyright (c) 2025 Akunuri Arun Deepak

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.



## 📫 Contact

For questions, feedback, or collaboration, feel free to reach out:

**Akunuri Arun Deepak**  
📧 Email: [arundeepak.akunuri@gmail.com](mailto:arundeepak.akunuri@gmail.com)

---

I’m happy to help with any inquiries related to this project!

